# Configure WSL

There is txo different way to configure WSL

* globally across all WSL distributions
* on a per-distribution basis

## Global Configuration

Edit your .wslconfig which is store on widows in %UserProfile%

```PowerShell
code %UserProfile%/.wslconfig
```

Many WSL2 (and Experimental) settings can be set, and the more important are the one to manage the processor and memory used by the WSL.
By default WSL will take

* The same number of logical processors on Windows
* 50% of total memory on Windows or 8GB.

Setting the processors and cpu properly is very important and depends of the loads of work you need to do in the WSL distribution.

Here is an example of a configuration for a WSL distribution on a 32GB RAM and 16 Logical processor computer; which will:

* Have several Podman containers (database, blod storage, queue, keycloak, ...)
* Run NX cli, Angular cli, Nest cli, python, pandas, ...
* Load large files

### For more information

* [Configuration setting for .wslconfig](https://learn.microsoft.com/en-us/windows/wsl/wsl-config#configuration-setting-for-wslconfig)

```env
# Settings apply across all Linux distros running on WSL 2
[wsl2]

# Limits VM memory to use no more than 12 GB
# Default is 50% of total memory on Windows or 8GB, whichever is less
memory=12GB # up to 16GB is needed

# Sets amount of swap storage space to 8GB
# Default is 25% of available RAM
# swap=8GB # up to 12GB is needed

# Sets the VM to use X virtual processors
# Default is the same number of logical processors on Windows
# processors=X
```

## per-distribution Configuration

> [!WARNING]
> BE CAREFUL WITH THIS CONFIGURATION !!!
> Usually not modified, because it is fine tuned by Microsoft for a a specific WSL distribution.

Here is the settings used in the WSL Ubuntu-20.04 distribution:

### For more information

* [Configuration settings for wsl.conf](https://learn.microsoft.com/en-us/windows/wsl/wsl-config#configuration-settings-for-wslconf)

```env
# Automatically mount Windows drive when the distribution is launched
[automount]

# Set to true will automount fixed drives (C:/ or D:/) with DrvFs under the root directory set above. Set to false means drives won't be mounted automatically, but need to be mounted manually or with fstab.
enabled = true

# Sets the directory where fixed drives will be automatically mounted. This example changes the mount location, so your C-drive would be /c, rather than the default /mnt/c. 
root = /

# DrvFs-specific options can be specified.  
options = "metadata,uid=1003,gid=1003,umask=077,fmask=11,case=off"

# Sets the `/etc/fstab` file to be processed when a WSL distribution is launched.
mountFsTab = true

# Network host settings that enable the DNS server used by WSL 2. This example changes the hostname, sets generateHosts to false, preventing WSL from the default behavior of auto-generating /etc/hosts, and sets generateResolvConf to false, preventing WSL from auto-generating /etc/resolv.conf, so that you can create your own (ie. nameserver 1.1.1.1).
[network]
hostname = DemoHost
generateHosts = false
generateResolvConf = false

# Set whether WSL supports interop process like launching Windows apps and adding path variables. Setting these to false will block the launch of Windows processes and block adding $PATH environment variables.
[interop]
enabled = false
appendWindowsPath = false

# Set the user when launching a distribution with WSL.
[user]
default = DemoUser

# Set a command to run when a new WSL instance launches. This example starts the Docker container service.
[boot]
command = service docker start
```

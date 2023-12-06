
# Prerequisites

You must be running Windows 10 version 2004 and higher (Build 19041 and higher) or Windows 11.

# Why

The Windows Subsystem for Linux (WSL) lets you run a Linux environment, including command-line tools and applications, directly on Windows, without the overhead of a traditional virtual machine or dual boot setup.

WSL especially helps web developers and those working with Bash and Linux-first tools (for example, Ruby and Python) to use their tools on Windows and ensure consistency between development and production environments.

There is 2 version of WSL, it is recommanded to use WSL 2:
* WSL 2 install a linux kernel inside a managed virtual machine (through a subset of Hyper-V features) that implements the full Linux kernel.
* WSL 1 had lot of performance issue because not all syscalls were implemented

# Install and configure Windows tools

* [Install VS Code](https://code.visualstudio.com/download)
* [Install and get started setting up Windows Terminal](https://learn.microsoft.com/en-us/windows/terminal/install)
* [Install and configure PowerShell](install-configure-PS.md)
* [Set up a custom prompt for PowerShell or WSL with Oh My Posh](https://github.com/CedricCazin/tutorials/blob/main/001%20-%20setup%20WSL%20development%20environment/README.md)

# Install and configure a WSL distribution

* [Install WSL](install-WSL.md)
* [Update and Install packages in WSL distribution](update-install-packages-WSL.md)
* [Configure WSL](configure-WSL.md)
* [Configure Terminal for WSL](configure-terminal-for-WSL.md)
* [configure VS Code in WSL](todo.md)

# Install and configure Unix Shell on a WSL distribution

* [Install and configure ZSH in WSL](install-configure-zsh.md)
* [install and configure oh-my-zsh in WSL](install-configure-oh-my-zsh.md)

# Install and configure Tools on a WSL distribution

> [!NOTE]
> When you are happy with a WSL distribution (configurations, shells, tools, ...),
> BACKUP IT to you can restore it quickly if anything happens

> [!WARNING]
> If you plan to share the backup,
> DO NOT create SSH KEYS or ser sensitive information before the backup
 
* [Install and configure GIT in WSL](install-configure-git.md)
* [Install and configure NodeJs with NVM in WSL](install-configure-nodejs-with-nvm.md)
* [🚧 Install and configure docker in WSL](todo.md)
* [🚧 Install and configure docker desktop Windows in WSL](todo.md)
* [🚧 Install and configure podman in WSL](todo.md)
* [🚧 Install and configure Python in WSL (side by side)](todo.md)
* [🚧 Install and configure Conda in WSL](todo.md)
* [🚧 Install and configure Poetry in WSL](todo.md)
* [🚧 Install and configure Terraform with TFN in WSL](todo.md)

# Backup/Restore a WSL distribution

* [Backup/Restore WSL distribution](backup-retore-WSL.md)

# For more installation guide 

please [Create an Issue](https://github.com/CedricCazin/tutorials/issues/new)
  

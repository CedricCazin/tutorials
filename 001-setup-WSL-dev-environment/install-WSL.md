# Install and Configure WSL

## Update WSL

If you already have WSL installed you should update the WSL.

```PowerShell
wsl --update
```

![image](https://github.com/CedricCazin/tutorials/assets/26877462/8dac2785-d90e-4833-8159-9943d03d6988)

## Install WSL

List the Linux distribution available.

```PowerShell
wsl --list --online
```

![image](https://github.com/CedricCazin/tutorials/assets/26877462/1eab0da7-5156-4d42-9806-5023b14ad48c)

Choose a distribution, and install it.

```PowerShell
wsl --install --distribution <distribution>
```

![image](https://github.com/CedricCazin/tutorials/assets/26877462/5ebaa49d-af5c-488c-969e-4410b0a29c7f)

## Configure WSL

On another terminal, you can list the installed distributions.

```PowerShell
wsl --list --verbose
```

![image](https://github.com/CedricCazin/tutorials/assets/26877462/4b52f93f-cad3-44a6-b591-fa8dbcf59749)

The distribution with a star(*) is the default distribution when you just type ```wsl``` in a terminal.
But you can change the default distribution with the following command.

```PowerShell
wsl --set-default <distribution>
```

![image](https://github.com/CedricCazin/tutorials/assets/26877462/fd193544-6231-4a0f-ba1c-e2a5a1de9f3c)

> [!IMPORTANT]
> The version of WSL should be 2, it provide more features [Comparing WSL 1 and WSL 2](https://learn.microsoft.com/en-us/windows/wsl/compare-versions).

To change the WSL version use the command:

```PowerShell
wsl --set-version <distribution> 2
```

## Shutdown

WSL take by default 50% of total memory on Windows or 8GB.
You can change how much WSL memory will take on start, see [Configure WSL](configure-WSL.md).
If you finished working on WSL, You might want to stop WSL to allocate this memory.

It is like a computer you need to terminate either one/several distribution.

```PowerShell
wsl --terminate <distribution> 
```

Or shutdown the whole WSL

```PowerShell
wsl --shutdown
```

## Help

To get help by the cli, type:

```PowerShell
wsl --help
```

## For more information

* [Install WSL](https://learn.microsoft.com/en-us/windows/wsl/install)
* [Basic commands for WSL](https://learn.microsoft.com/en-us/windows/wsl/basic-commands)
* [Training – Introduction to Windows Subsystem for Linux (WSL)](https://learn.microsoft.com/en-us/training/modules/wsl-introduction)

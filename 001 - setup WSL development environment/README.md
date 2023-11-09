
# Prerequisites

You must be running Windows 10 version 2004 and higher (Build 19041 and higher) or Windows 11.

# Install WSL

List the Linux distribution available.

```PowerShell
wsl --list --online
```

![image](https://github.com/CedricCazin/tutorials/assets/26877462/1eab0da7-5156-4d42-9806-5023b14ad48c)

Choose a distribution, and install it.

```PowerShell
wsl --install --distribution <ditribution>
```

![image](https://github.com/CedricCazin/tutorials/assets/26877462/5ebaa49d-af5c-488c-969e-4410b0a29c7f)

# Update WSL

If you already have WSL installed you should update the WSL.

```PowerShell
wsl --update
```

![image](https://github.com/CedricCazin/tutorials/assets/26877462/8dac2785-d90e-4833-8159-9943d03d6988)

# Configure WSL

On another terminal, you can list the installed distributions.

```PowerShell
wsl --list --verbose
```

![image](https://github.com/CedricCazin/tutorials/assets/26877462/4b52f93f-cad3-44a6-b591-fa8dbcf59749)

The distribution with a star(*) is the default distribution when you just type ```wsl``` in a terminal.
But you can change the default distribution with the following command.

```PowerShell
wsl --set-default <ditribution>
```

![image](https://github.com/CedricCazin/tutorials/assets/26877462/fd193544-6231-4a0f-ba1c-e2a5a1de9f3c)

> [!IMPORTANT]
> The version of WSL should be 2, it provide more features [Comparing WSL 1 and WSL 2](https://learn.microsoft.com/en-us/windows/wsl/compare-versions).

To change the WSL version use the command:

```PowerShell
wsl --set-version <distribution> 2
```

# Help

To get help by the cli, type:

```PowerShell
wsl --help
```

For more information check Microsoft documentations:

* [Install WSL](https://learn.microsoft.com/en-us/windows/wsl/install)
* [Basic commands for WSL](https://learn.microsoft.com/en-us/windows/wsl/basic-commands)

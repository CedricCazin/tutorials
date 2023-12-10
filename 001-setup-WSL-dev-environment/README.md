# Setup a WSL dev environment

## Prerequisites

You must be running Windows 10 version 2004 and higher (Build 19041 and higher) or Windows 11.

## Why

The Windows Subsystem for Linux (WSL) lets you run a Linux environment, including command-line tools and applications, directly on Windows, without the overhead of a traditional virtual machine or dual boot setup.

WSL especially helps web developers and those working with Bash and Linux-first tools (for example, Ruby and Python) to use their tools on Windows and ensure consistency between development and production environments.

There is 2 version of WSL, it is recommanded to use WSL 2:

* WSL 2 install a linux kernel inside a managed virtual machine (through a subset of Hyper-V features) that implements the full Linux kernel.
* WSL 1 had lot of performance issue because not all syscalls were implemented

## Install and configure Windows tools

* [Install VS Code](https://code.visualstudio.com/download)

Optional but highly recommended:

* Windows Terminal \
  [Install and get started setting up Windows Terminal](https://learn.microsoft.com/en-us/windows/terminal/install)

* PowerShell \
  [Install PowerShell](https://learn.microsoft.com/en-us/powershell/scripting/install/installing-powershell-on-windows) \
  [Get PowerShell 7](https://github.com/PowerShell/PowerShell/blob/master/README.md#get-powershell)

* Oh My Posh \
  [Customize your PowerShell prompt with Oh My Posh](https://learn.microsoft.com/windows/terminal/tutorials/custom-prompt-setup#customize-your-powershell-prompt-with-oh-my-posh) \
  [Install a Nerd font](https://learn.microsoft.com/en-us/windows/terminal/tutorials/custom-prompt-setup#install-a-nerd-font) \
  [Use Terminal-Icons to add missing folder or file icons](https://learn.microsoft.com/en-us/windows/terminal/tutorials/custom-prompt-setup#use-terminal-icons-to-add-missing-folder-or-file-icons)

Your Powershell in Windows Terminal should look like this, nice 😉

![image](https://github.com/CedricCazin/tutorials/assets/26877462/33745a60-b054-4af5-a698-a75cf66a652e)

## Install and configure a WSL distribution

* [Install WSL](install-WSL.md)
* [Configure WSL](configure-WSL.md)
* [Configure Terminal for WSL](configure-terminal-for-WSL.md)
* [Configure VSCode for WSL](configure-vscode-for-wsl.md)

## Backup/Restore a WSL distribution

* [Backup/Restore WSL distribution](backup-retore-WSL.md)

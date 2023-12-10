
# Prerequisites

* [Update and Install packages in WSL distribution](update-install-packages-WSL.md)

# What is ZSH

Zsh or Z shell is a Unix shell extended from extended Bourne shell.

# Install ZSH

```sh
sudo apt install zsh
```

For more information check Microsoft documentations:

* [Install ZSH on WSL ubuntu](https://github.com/ohmyzsh/ohmyzsh/wiki/Installing-ZSH#ubuntu-debian--derivatives-windows-10-wsl--native-linux-kernel-with-windows-10-build-1903)

# Set ZSH as default shell

Use [chsh](https://manpages.ubuntu.com/manpages/focal/en/man1/chsh.1.html)

```sh
chsh -s $(which zsh)
```

# Configure ZSH

When there is no ~/.zshrc file, ZSH will porpose a configuration workflow.

![image](https://github.com/CedricCazin/tutorials/assets/26877462/d2abccdd-0312-4280-bd55-4f9ecc600581)

In our case, Select 0.
Configuration of ZSH will be done with oh-my-zsh.

# Common Shell Bonus

* Shorthand are shorter (to type) of an option like -h for --help.
* Everything is case sensitive.
* ~ is for home

* # user is admin

* $ user is normal

## ZSH informations

Like on bash the standard information are displayed

* the current path
* the user
* the computer
  
But with ZSH other information can be found like:

* the current OS as an icon
* the git branch, number of files modified, number of commit to push, ...
* the execution time of the latest command
* ...

![image](https://github.com/CedricCazin/tutorials/assets/26877462/02b8c090-9fc2-4294-89e7-fe8b54dbec2f)

## To seek help on a command

```sh
# Manual page
man ls

# shorthand option for help
npm -h

# option for help
npm --help
```

## Piping commands & | >

Pipe is used to combine the output of a first command to another one.

```sh
# save the output of the ls to a file
ls -la > myfile.txt

# List the possible npm run scripts than grep the line containing ser
npm run | grep ser
```

# Chaining commands with conrol operators && and ||

Control operators help to continue commands based on the result of the first command.

```sh
# export the env variable and serve
export DB_CONECT_URI=lalalal && npm run serve

# serve anly if the build is sucessfull
npm run build || npm run serve
```

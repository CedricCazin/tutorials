# GIT

## Prerequisites

Update the distribution packages

```sh
sudo apt update && sudo apt upgrade
```

## Install

Git come already installed in Ubuntu, but you may want to update to the latest version.

```sh
sudo apt-get install git-all
```

## Configure

To avoid problems in your diffs, you can configure Git to properly handle line endings.

```sh
git config --global core.autocrlf true
```

You can change the text editor by Git (for interactive rebase...):

```sh
git config --global core.editor "code --wait"
```

You check your git configuration on the file **"~/.gitconfig"**.

## Create a ssh key (for github)

> [!WARNING]
> IF YOU PLAN TO BACKUP YOUR WSL FOR SHARING PURPOSE,
> DO NOT CREATE THE SSH KEYS NOW, BUT DO IT AFTER THE BACKUP

There is 2 ways to wotk with Github:

* HTTPS
* SSH

In WSL, there is a tool to generate keys

```sh
ssh-keygen -t < rsa -b 4096  | ed25519 > -C < name of your key >
```

Copy the ssh public key

```sh
cat ~/.ssh/id_rsa.pub
```

Add it to your github settings SSH keys

[Github Settings Keys](https://github.com/settings/keys)

Check if the ssh-agent is running

```sh
eval `ssh-agent -s`
```

Add your ssh key to the ssh-agent

```sh
ssh-add ~/.ssh/id_rsa
```

## Setup your global info

```sh
git config --global user.name "< your name here >"
git config --global user.email "< your email here >"
```

## For more information

* [Github Getting started with Git](https://docs.github.com/en/get-started/getting-started-with-git)
* [Connecting to Github with SSH](https://docs.github.com/en/authentication/connecting-to-github-with-ssh)
* [Associating VS Code with Git](https://docs.github.com/en/get-started/getting-started-with-git/associating-text-editors-with-git#using-visual-studio-code-as-your-editor)

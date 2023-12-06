# Install GIT

Git come already installed in Ubuntu, but you may wanto to update to the latest version.

```sh
sudo apt-get install git
```

You can change the text editor by Git (for interractive rebase...):

```sh
git config --global core.editor "code --wait"
```

# Create a ssh key (for github)

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

For more information check Github documentations:

* [Github Getting started with Git](https://docs.github.com/en/get-started/getting-started-with-git)
* [Connecting to Github with SSH](https://docs.github.com/en/authentication/connecting-to-github-with-ssh)

# Setup your global info

```sh
git config --global user.name "< your name here >"
git config --global user.email "< your email here >"
```

For more information check Github documentations:

* [Associating VS Code with Git](https://docs.github.com/en/get-started/getting-started-with-git/associating-text-editors-with-git#using-visual-studio-code-as-your-editor)

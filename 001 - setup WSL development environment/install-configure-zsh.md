
# Prerequisites

Update the distribution packages

```sh
sudo apt update && sudo apt upgrade
```

# Install ZSH

```sh
sudo apt install zsh
```

For more information check Microsoft documentations:

* [Install ZSH on WSL ubuntu ](https://github.com/ohmyzsh/ohmyzsh/wiki/Installing-ZSH#ubuntu-debian--derivatives-windows-10-wsl--native-linux-kernel-with-windows-10-build-1903)

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

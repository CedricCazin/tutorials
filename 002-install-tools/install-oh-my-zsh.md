# oh-my-zsh

Oh My Zsh is a delightful, open source, community-driven framework for managing your Zsh configuration. It comes bundled with thousands of helpful functions, helpers, plugins, themes, and a few things that make you shout...

## Prerequisites

* [Install and configure ZSH in WSL](install-configure-zsh.md)

Update the distribution packages

```sh
# Update packages repository
sudo apt update && sudo apt upgrade
```

## Install oh-my-zsh

Install oh-my-zsh using curl, wget or other methods

```sh
sh -c "$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
```

![image](https://github.com/CedricCazin/tutorials/assets/26877462/aad27023-d399-48ad-b19a-0d01eab33758)

### For more information

* [oh-my-zsh - Basic Installation](https://github.com/ohmyzsh/ohmyzsh#basic-installation)

## Configure oh-my-zsh

Open the ZSH configuration file with VS Code

```sh
code ~/.zshrc
```

## Plugins

oh-my-zsh propose LOTS of plugins (thanks to the community)
Just add them in the ~/.zshrc file.

```bash
plugins=(
  history aliases themes emoji
  git dotenv
  nvm node npm gulp grunt
  ng dotnet
  podman docker docker-compose
  python pip pyenv poetry
  terraform aws azure kubectl kubectx
)
```

### For more information

* [oh-my-zsh - plugins](https://github.com/ohmyzsh/ohmyzsh/wiki/Plugins)

## zsh-autosuggestions

git clone zsh-autosuggestions repo in you oh-my-zsh plugins folder.

```sh
git clone --depth=1 https://github.com/zsh-users/zsh-autosuggestions ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-autosuggestions

```

Add it in the plugins list of the ~/.zshrc file.

```bash
plugins=( \
  # other plugins...
  zsh-autosuggestions
)
```

### For more information

* [zsh-autosuggestions - install for oh-my-zsh](https://github.com/zsh-users/zsh-autosuggestions/blob/master/INSTALL.md#oh-my-zsh)

## zsh-syntax-highlighting

git clone zsh-autosuggestions repo in you oh-my-zsh plugins folder.

```sh
git clone https://github.com/zsh-users/zsh-syntax-highlighting.git ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-syntax-highlighting
```

Add it in the plugins list of the ~/.zshrc file.

```bash
plugins=( \
  # other plugins...
  zsh-syntax-highlighting
)
```

## Themes

oh-my-zsh propose several themes, select one and set the name in the ~/.zshrc file.

```bash
ZSH_THEME=robbyrussell
```

### For more information

* [oh-my-zsh - Themes](https://github.com/ohmyzsh/ohmyzsh/wiki/Themes)

## Powerlevel10k theme

git clone powerlevel10k repo in you oh-my-zsh themes folder and configure by following the wizard using this command line

```sh
git clone --depth=1 https://github.com/romkatv/powerlevel10k.git ${ZSH_CUSTOM:-$HOME/.oh-my-zsh/custom}/themes/powerlevel10k
```

Add in the ~/.zshrc file the following line, restart the shell and follow the wizard 🧙‍♂️

```bash
ZSH_THEME="powerlevel10k/powerlevel10k" in ~/.zshrc.
```

At any time if you want to change the configuration of the theme, just lauch:

```sh
p10k configure
```

### For more information

* [Powerlevel10k - oh-my-zsh - Installation](https://github.com/romkatv/powerlevel10k#oh-my-zsh)

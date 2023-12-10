# NVM

nvm is a version manager for node.js, designed to be installed per-user, and invoked per-shell. nvm works on any POSIX-compliant shell (sh, dash, ksh, zsh, bash), in particular on these platforms: unix, macOS, and windows WSL.

## Prerequisites

Update the distribution packages

```sh
# Update packages repository
sudo apt update && sudo apt upgrade

# Install needed packages
sudo apt curl -y
```

## Install

nvm is a version manager for node.js, which help you install several versions of node.js and and switch between version as you wish.

```sh
curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.5/install.sh | bash

# or

wget -qO- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.5/install.sh | bash
```

## Configure

Nvm need to be present in your shell profile file (~/.bashrc, ~/.zshrc, ...)

```sh
export NVM_DIR="$([ -z "${XDG_CONFIG_HOME-}" ] && printf %s "${HOME}/.nvm" || printf %s "${XDG_CONFIG_HOME}/nvm")"
[ -s "$NVM_DIR/nvm.sh" ] && \. "$NVM_DIR/nvm.sh" # This loads nvm
```

## Usage

After restarting your shel you can use nvm like so:

### List the available node.js version to be installed

```sh
nvm ls-remote
```

### List node.js version

List installed version, \
Used and default versions, \
available lts and the latest stable to be installed (if nvm ls-remote has been done prior).

```sh
nvm list
```

![image](https://github.com/CedricCazin/tutorials/assets/26877462/aebdbb4c-7ae8-4a2a-9c49-0b8ccf5b6904)

### Install node.js version

```sh
# "node" is an alias for the latest version
nvm install node

# "lts/hydrogen" is an alias for the lts 18 version
nvm install lts/hydrogen

# specific version
nvm install 20.9.0
```

### Use a node.js version

```sh
# "node" is an alias for the latest version
nvm use node

# "lts/hydrogen" is an alias for the lts 18 version
nvm use lts/hydrogen

# specific version
nvm use 20.9.0
```

## For more information

* [NVM](https://github.com/nvm-sh/nvm)
* [NVM Install](https://github.com/nvm-sh/nvm#install--update-script)
* [NVM Usage](https://github.com/nvm-sh/nvm#usage)

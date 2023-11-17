
# Prerequisites

Enter the WSL distribution

# Update packages

Update the distribution packages

```sh
sudo apt update && sudo apt upgrade
```

# Install packages

The packages to install depends en which tools you need to install, But this ones are commonly used.

```sh
sudo apt-get install -y \
    git-all \
    bzip2 \
    jq \  
    iptables \
    unzip \
    wget \
    zlib1g \
    libssl-dev \
    zlib1g-dev \
    libnghttp2-dev \
    curl
```

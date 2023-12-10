# Install GIT

## Prerequisites

Update the distribution packages

```sh
# Update packages repository
sudo apt update && sudo apt upgrade

# Install needed packages
sudo apt install apt-transport-https ca-certificates curl software-properties-common -y
```

## Add Docker repository

```sh
# Add Docker repository GPG key
sudo apt-get update
sudo apt-get install ca-certificates curl gnupg
sudo install -m 0755 -d /etc/apt/keyrings
curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo gpg --dearmor -o /etc/apt/keyrings/docker.gpg
sudo chmod a+r /etc/apt/keyrings/docker.gpg

# Add Docker repository
echo \
  "deb [arch=$(dpkg --print-architecture) signed-by=/etc/apt/keyrings/docker.gpg] https://download.docker.com/linux/ubuntu \
  $(. /etc/os-release && echo "$VERSION_CODENAME") stable" | \
  sudo tee /etc/apt/sources.list.d/docker.list > /dev/null
  
sudo apt-get update
```

## Install manually

Install Docker by running:

```sh
sudo apt-get install docker-ce docker-ce-cli containerd.io docker-buildx-plugin docker-compose-plugin
```

Check that Docker is running:

```sh
sudo systemctl status docker
```

## Install with convenience script

Docker provides a convenience script at <https://get.docker.com/> to install Docker into development environments non-interactively.

```sh
curl -fsSL https://get.docker.com -o get-docker.sh
sudo sh ./get-docker.sh --dry-run
```

## Using Docker and Docker Compose

```sh
# Docker help
docker --help

# Docker Compose help
docker compose --help
```

## For more information check Docker documentations

* <https://docs.docker.com/engine/install/ubuntu/>

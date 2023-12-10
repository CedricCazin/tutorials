# Podman

Podman Desktop is an open source graphical tool enabling you to seamlessly work with containers and Kubernetes from your local environment.

## Prerequisites

Update the distribution packages

```sh
# Update packages repository
sudo apt update && sudo apt upgrade

# Install needed packages
sudo apt install apt-transport-https ca-certificates curl software-properties-common -y
```

## Install manually

Install podman on Ubuntu 20.10 and newer

```sh
sudo apt-get update
sudo apt-get -y install podman
```

Install podman on Ubuntu 20.09 and previous

```sh
sudo mkdir -p /etc/apt/keyrings

curl -fsSL "https://download.opensuse.org/repositories/devel:kubic:libcontainers:stable/xUbuntu_$(lsb_release -rs)/Release.key" \
  | gpg --dearmor \
  | sudo tee /etc/apt/keyrings/devel_kubic_libcontainers_stable.gpg > /dev/null

echo \
  "deb [arch=$(dpkg --print-architecture) signed-by=/etc/apt/keyrings/devel_kubic_libcontainers_stable.gpg]\
    https://download.opensuse.org/repositories/devel:kubic:libcontainers:stable/xUbuntu_$(lsb_release -rs)/ /" \
  | sudo tee /etc/apt/sources.list.d/devel:kubic:libcontainers:stable.list > /dev/null

sudo apt-get update -qq

sudo apt-get -qq -y install podman
```

## Using Docker and Docker Compose

```sh
# Podman help
podman --help

# Podman Compose help
# ONLY ON Podman 4.7.0 (Ubuntu 22.04) or greater
podman compose --help
```

## For more information

* <https://podman.io/docs/installation>

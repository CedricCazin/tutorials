
Ubuntu_20.04

echo "deb https://download.opensuse.org/repositories/devel:/kubic:/libcontainers:/stable/xUbuntu_20.04/ /" | sudo tee /etc/apt/sources.list.d/devel:kubic:libcontainers:stable.list

curl -L "https://download.opensuse.org/repositories/devel:/kubic:/libcontainers:/stable/xUbuntu_20.04/Release.key" | sudo apt-key add -

sudo apt install -y \
    slirp4netns \
    buildah \
    podman

> Ubuntu_20.04

sudo apt-get -y install podman

https://podman.io/docs/installation

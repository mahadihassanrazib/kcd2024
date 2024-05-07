# Hello Dhaka! Welcome to the KCD Dhaka 2024!

## Please follow step by step installation and application run process for Tracing Demo

# minimum hardware requirement

```bash
CPU: 4 Core
RAM: 8GB
Storage: 30GB
```

### Installing VirtualBox on Ubuntu OS / Windows WSL2 Ubuntu

```bash
# Select the VirtualBox package for your Ubuntu version and download it from the provided link.

# For Ubuntu 22.04: Download VirtualBox 7.0.18 for Ubuntu 22.04
https://download.virtualbox.org/virtualbox/7.0.18/virtualbox-7.0_7.0.18-162988~Ubuntu~jammy_amd64.deb

# or

# For Ubuntu 20.04: Download VirtualBox 7.0.18 for Ubuntu 20.04
https://download.virtualbox.org/virtualbox/7.0.18/virtualbox-7.0_7.0.18-162988~Ubuntu~focal_amd64.deb

# Install the downloaded VirtualBox package for ubuntu 22.04 using the dpkg command.
sudo dpkg -i virtualbox-7.0_7.0.18-162988~Ubuntu~jammy_amd64.deb

# or

# Install the downloaded VirtualBox package for ubuntu 20.04 using the dpkg command.
sudo dpkg -i virtualbox-7.0_7.0.18-162988~Ubuntu~focal_amd64.deb
```
### Install Virtualbox on MacOS
Install Virtualbox for MacOS using homebrew
```bash
brew install --cask virtualbox
```

### Installing Vagrant with HashiCorp Repository on Ubuntu OS / Windows WSL2 Ubuntu

```bash
# Download the HashiCorp GPG key and save it as a file named hashicorp-archive-keyring.gpg in the /usr/share/keyrings directory.
wget -O- https://apt.releases.hashicorp.com/gpg | sudo gpg --dearmor -o /usr/share/keyrings/hashicorp-archive-keyring.gpg

# Add HashiCorp's Debian repository to the list of package sources. The signed-by option specifies the keyring file for signature verification.
echo "deb [signed-by=/usr/share/keyrings/hashicorp-archive-keyring.gpg] https://apt.releases.hashicorp.com $(lsb_release -cs) main" | sudo tee /etc/apt/sources.list.d/hashicorp.list

# Update the list of available packages and install Vagrant from the HashiCorp repository.
sudo apt update && sudo apt install vagrant
```

### Install Vagrant on MacOS
Install Vagrant for MacOS using homebrew
```bash
brew tap hashicorp/tap
brew install hashicorp/tap/hashicorp-vagrant
```

## After installation complete restart your computer


```bash
# Now go into vagrant folder of the repo.
cd vagrant/
# Change between 62 to 70 number line according to your Hardware capacity

# run vagrant server wait until finish the vagrant server setup
vagrant up

# now get into ubuntu server with the command of
vagrant ssh

## with this run it will install Docker, Minikube and Kubectl software tools in Ubuntu 20.04 Server.

```

## Before START minikube

```bash
sudo usermod -aG docker $USER && newgrp docker

# start minikube (Kubernetes environment) with this command

minikube start --kubernetes-version=v1.29.4 --nodes 1 --cpus 4 --memory 4096 --disk-size 25g --driver=docker

# After installation finished check minikube node and running pods by

kubectl get nodes

# get pods within all namespace

kubectl get pods -A

```

## Congratulations finally you setup a fully functional Kubernetes Cluster! Best of Luck 👍

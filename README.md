# Hello Dhaka! Welcomes the Future of Tech KCD 2024!

## Please follow step by step installation and application run process for Tracing Demo


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

### Installing Vagrant with HashiCorp Repository on Ubuntu OS / Windows WSL2 Ubuntu

```bash
# Download the HashiCorp GPG key and save it as a file named hashicorp-archive-keyring.gpg in the /usr/share/keyrings directory.
wget -O- https://apt.releases.hashicorp.com/gpg | sudo gpg --dearmor -o /usr/share/keyrings/hashicorp-archive-keyring.gpg

# Add HashiCorp's Debian repository to the list of package sources. The signed-by option specifies the keyring file for signature verification.
echo "deb [signed-by=/usr/share/keyrings/hashicorp-archive-keyring.gpg] https://apt.releases.hashicorp.com $(lsb_release -cs) main" | sudo tee /etc/apt/sources.list.d/hashicorp.list

# Update the list of available packages and install Vagrant from the HashiCorp repository.
sudo apt update && sudo apt install vagrant

```

## After installation complete restart your computer


### Now go into vagrant folder of the repo.



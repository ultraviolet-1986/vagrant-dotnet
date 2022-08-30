# -*- mode: ruby -*-
# vi: set ft=ruby :

# Author: William Whinn
# Date: 30th August 2022

# NOTES
# - Based on Ubuntu 22.04 LTS.
# - Intended to develop Dotnet Core applications.
 
Vagrant.configure("2") do |config|
  config.vm.box = "ubuntu/jammy64"

  config.vm.hostname = "ubuntu-vagrant"

  config.vm.network "private_network", ip: "192.168.56.111"

  config.vm.provider "virtualbox" do |vb|
    vb.name = "Ubuntu 22.04 LTS (Vagrant)"
    vb.cpus = 2
    vb.memory = 2048
  end

  config.vm.synced_folder "../Documents/Workspace/git", "/host"

  # Update/install software in VM.
  config.vm.provision "shell", inline: <<-SCRIPT
    sudo apt update
    sudo apt full-upgrade -y
    sudo apt install -y build-essential curl dotnet6 git nano snapd vim
    sudo snap refresh
  SCRIPT
end

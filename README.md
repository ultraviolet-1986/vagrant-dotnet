# Vagrant Dotnet VM

A Dotnet development VM for Vagrant based on Ubuntu 22.04 LTS

## Introduction

This `Vagrantfile` is intended to allow a user to build and run
[Dotnet](https://dotnet.microsoft.com/en-us/) applications without requiring
this software to be installed on the host machine. Note that this VM will be
provisioned using [Oracle VM VirtualBox](https://www.virtualbox.org/), which
should be installed along with [Vagrant](https://www.vagrantup.com/) and is
based on the [Ubuntu Linux](https://ubuntu.com/) operating system.

## Instructions

These instructions assume that the user has already cloned this repository into
a directory of their choice and that the directory `~/Documents/Workspace/git`
exists.

1. Open a Terminal within the directory of the `Vagrantfile`.
2. Use the command `vagrant up` to create and run the Virtual Machine.
3. Once the VM has been updated and built, use the command `vagrant ssh` to log
   in to the container.
4. It should be possible to navigate the shared file-system on the host machine
   by navigating to the
   `/host` directory within the VM.
5. From your chosen directory, you may use the following commands to run your C#
   project: `dotnet clean`, `dotnet build`, and `dotnet run`. Run these each
   time to ensure a fresh build.
6. It is possible to stop the VM by using the command `vagrant halt` on the host
   Terminal.
7. To delete the VM, use the command `vagrant destroy` on the host Terminal.

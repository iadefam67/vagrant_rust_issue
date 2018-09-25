# Setting up a virtual machine for Rust projects with Vagrant/VirtualBox

I ran into some issues using Vagrant to install Rust into a virtual machine, using an inline bash script in the otherwise default Vagrantfile. The corrected Vagrantfile is in this repository, along with an outline of the steps I followed to get this up and running. 

1. Follow the Vagrant [Getting Started guide](https://www.vagrantup.com/intro/getting-started/). Use the VirtualBox instructions for your virtual machine provider. 
1. Once you have both Vagrant and Virtual Box installed, used the Vagrantfile in this repository (you can just replace your default file). 
1. Run `vagrant up` to create the virtual machine. You should see output messages confirming that Rust has installed. 
1. Run `vagrant ssh` to enter the virtual machine. Run `ls -la` and make sure you have a `.cargo` directory installed to `/home/vagrant`. If not, something went wrong with the installation. 
1. Run `rustc --version` to confirm that your $PATH has been configured correctly for Rust commands to execute. You should see the Rust version that you have installed listed. If not, start googling. 

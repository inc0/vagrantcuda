# -*- mode: ruby -*-
# vi: set ft=ruby :

# All Vagrant configuration is done below. The "2" in Vagrant.configure
# configures the configuration version (we support older styles for
# backwards compatibility). Please don't change it unless you know what
# you're doing.
Vagrant.configure("2") do |config|
  config.vm.box = "ubuntu/xenial64"

   config.vm.provider "virtualbox" do |vb|
     # Display the VirtualBox GUI when booting the machine
     vb.gui = "false"

     # Customize the amount of memory on the VM:
     vb.memory = "12288"
     vb.customize ["modifyvm", :id, "--chipset", "ich9", "--pciattach", "2:00.0@2:00.0"]
   end

  config.vm.provision "ansible" do |ansible|
    ansible.playbook = "setup_cuda.yml"
  end

end

# -*- mode: ruby -*-
# vi: set ft=ruby :

# All Vagrant configuration is done below. The "2" in Vagrant.configure
# configures the configuration version (we support older styles for
# backwards compatibility). Please don't change it unless you know what
# you're doing.
Vagrant.configure("2") do |config|
  config.vm.box = "xenial"

  config.vm.provider :libvirt do |domain|
    domain.memory = 12288
    domain.cpus = 4
    domain.kvm_hidden = true
    domain.pcis = [{
        bus: 2,
        slot: 0,
        function: 0,
    }]
  end

  config.vm.provision "ansible" do |ansible|
    ansible.playbook = "setup_cuda.yml"
  end

end

# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure(2) do |config|

  config.vm.box = "ubuntu/trusty64"
  config.vm.provider "virtualbox" do |vb|
    config.vbguest.auto_update = true
    vb.customize ["modifyvm", :id, "\--memory", "6144"]
    vb.customize ["modifyvm", :id, "\--cpus", "2"]
  end

  # If you want to use this system to netboot Raspberry Pi, then uncomment this line
#  config.vm.network "public_network", bridge: 'ask', ip: "10.0.80.1"

  config.vm.provision "ansible" do |ansible|
    ansible.playbook = "playbook.yml"
  end
end

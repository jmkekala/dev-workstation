# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
  config.vm.box = "jmkekala/centos73"
  config.vm.hostname = "development"
  config.vm.synced_folder '.', '/vagrant', disabled: true

  config.vm.provider "hyperv" do |hv|
      hv.memory = "4096"
  end
  
  config.vm.provision "ansible" do |ansible|
    ansible.verbose = "v"
    ansible.playbook = "main.yml"
  end
end

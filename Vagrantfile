# -*- mode: ruby -*-
# vi: set ft=ruby :

UBUNTU_ENV = "ansible-docker-ubuntu"

Vagrant.configure(2) do |config|
  
  config.vm.define UBUNTU_ENV do |env|
    env.vm.box = "ubuntu/trusty64"
    
    env.vm.provider :virtualbox do |vb|
      vb.name = UBUNTU_ENV
      vb.cpus = 1
      vb.memory = 1024
    end

  end

  config.vm.provision :ansible do |ansible|
    ansible.playbook = 'tests/vagrant.yml'
  end

end

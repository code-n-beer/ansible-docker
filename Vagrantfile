# -*- mode: ruby -*-
# vi: set ft=ruby :

boxes = [ { name: "ubuntu", image: "ubuntu/trusty64" }, 
          { name: "debian", image: "debian/jessie64" } ]

Vagrant.configure(2) do |config|
  
  boxes.each do |box|
    box_name = "ansible-docker-#{box[:name]}"
    config.vm.define box_name do |env|
      env.vm.box = box[:image]
      env.vm.hostname = box_name

      env.vm.provider :virtualbox do |vb|
        vb.name = box_name
        vb.cpus = 1
        vb.memory = 1024
      end
    end
  end
  
  config.vm.provision :ansible do |ansible|
    ansible.playbook = 'tests/vagrant.yml'
  end

end

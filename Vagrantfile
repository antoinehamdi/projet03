# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|

  config.vm.box = "geerlingguy/centos7"

  config.vm.provider :virtualbox do |v|
        v.memory = 512
        v.linked_clone = true
    end

    # Machine 1
    config.vm.define "machine1" do |machine1|
        machine1.vm.hostname = "machine1"
        # static ip address
        machine1.vm.network :private_network, ip: "192.168.8.101"
        machine1.vm.provision "file", source: "~/.ssh/id_rsa.pub", destination: "~/.ssh/me.pub"
    end

        # Machine 1
    config.vm.define "machine2" do |machine2|
        machine2.vm.hostname = "machine2"
        # static ip address
        machine2.vm.network :private_network, ip: "192.168.8.102"
    end

    # Machine 3
    config.vm.define "machine3" do |machine3|
        machine3.vm.hostname = "machine3"
        # static ip address
        machine3.vm.network :private_network, ip: "192.168.8.103"
    end

end

# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
  config.vm.box = "centos/7"
  config.ssh.insert_key = false
  config.vm.synced_folder ".", "/vagrant", disabled: true
  config.vm.provider "virtualbox" do |vb|
     vb.memory = "256"
   end

  config.vm.define "master" do |master|
    master.vm.hostname = "master.dev"
    master.vm.network "private_network", ip: "192.168.33.10"
  end

  config.vm.define "replica1" do |replica|
    replica.vm.hostname = "replica1.dev"
    replica.vm.network "private_network", ip: "192.168.33.11"
  end

  config.vm.define "replica2" do |replica|
    replica.vm.hostname = "replica2.dev"
    replica.vm.network "private_network", ip: "192.168.33.12"
  end
end

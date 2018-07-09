# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
  config.vm.box = "centos/7"
  config.ssh.insert_key = false
  config.vm.synced_folder ".", "/vagrant", disabled: true
  config.vm.provider "virtualbox" do |vb|
     vb.memory = "256"
   end

  config.vm.define "dbsvr1" do |master|
    master.vm.hostname = "dbsvr1.dev"
    master.vm.network "private_network", type: "dhcp"
  end

  config.vm.define "dbsvr2" do |replica|
    replica.vm.hostname = "dbsvr2.dev"
    replica.vm.network "private_network", type: "dhcp"
  end

  config.vm.define "backupsvr" do |replica|
    replica.vm.hostname = "backupsvr.dev"
    replica.vm.network "private_network", type: "dhcp"
  end
end

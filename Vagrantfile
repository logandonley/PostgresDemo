# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
  config.vm.box = "geerlingguy/centos7"
  config.ssh.insert_key = false
  config.vm.synced_folder ".", "/vagrant", disabled: true
  config.vm.provider "virtualbox" do |vb|
     vb.memory = "256"
   end

  config.vm.define "demo" do |demo|
    demo.vm.hostname = "demo.dev"
    demo.vm.network "private_network", ip: "192.168.33.10"
  end
end

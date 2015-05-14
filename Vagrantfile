# -*- mode: ruby -*-
# vi: set ft=ruby :

VAGRANTFILE_API_VERSION = "2"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|
  config.vm.box = "trusty64"
  config.vm.box_url = "https://cloud-images.ubuntu.com/vagrant/trusty/current/trusty-server-cloudimg-amd64-vagrant-disk1.box"
  config.vm.provision "shell", inline: "echo Hello"

  config.ssh.insert_key = false

  config.vm.define "web" do |web|
    web.vm.box = "trusty64"
    web.vm.hostname = "web"
    web.vm.network "private_network", ip: "192.168.101.11"
  end

  config.vm.define "db" do |db|
    db.vm.box = "trusty64"
    db.vm.hostname = "db"
    db.vm.network "private_network", ip: "192.168.101.12"
  end
end


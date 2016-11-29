# -*- mode: ruby -*-
# vi: set ft=ruby :

VAGRANTFILE_API_VERSION = "2"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|
#  config.vm.box = "opscode-ubuntu-12.04"
  config.vm.box = "ansible-ubuntu-1204-i386"
  config.vm.box_url = "http://opscode-vm-bento.s3.amazonaws.com/vagrant/virtualbox/opscode_ubuntu-12.04-i386_chef-provisionerless.box"

  config.vm.define "control" do |control|
    control.vm.network :private_network, ip: "192.168.61.10"
  end

  config.vm.define "db" do |db|
    db.vm.network :private_network, ip: "192.168.61.11"
  end

  config.vm.define "dbel" do |db|
    db.vm.network :private_network, ip: "192.168.61.14"
    db.vm.box = "opscode_centos-6.5-i386"
  end

  config.vm.define "www" do |www|
    www.vm.network :private_network, ip: "192.168.61.12"
  end

  config.vm.define "lb" do |lb|
    lb.vm.network :private_network, ip: "192.168.61.13"
  end

end


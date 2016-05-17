# -*- mode: ruby -*-
# vi: set ft=ruby :

# All Vagrant configuration is done below. The "2" in Vagrant.configure
# configures the configuration version (we support older styles for
# backwards compatibility). Please don't change it unless you know what
# you're doing.
storage_disk = './tmp/openstack_storage_disk.vdi'

Vagrant.configure(2) do |config|

  config.ssh.insert_key = false

  config.vm.define "controller" do |instance|
    instance.vm.box = "centos/7"
    instance.vm.host_name = "controller"
    instance.vm.network "private_network", ip: "10.0.0.11", netmask: "255.255.255.0"
    instance.vm.network "private_network", ip: "192.168.50.11", netmask: "255.255.255.0"
    instance.vm.provider "virtualbox" do |vb|
      vb.memory = "2048"
      vb.cpus = 2
      vb.customize ["modifyvm", :id, "--natdnshostresolver1", "on"]
    end
    instance.vm.provision "shell", inline: <<-SHELL
        echo "10.0.0.11 controller" | sudo tee -a /etc/hosts
        echo "10.0.0.31 compute1" | sudo tee -a /etc/hosts
        echo "10.0.0.41 storage1" | sudo tee -a /etc/hosts
    SHELL
  end

  config.vm.define "compute1" do |instance|
    instance.vm.box = "centos/7"
    instance.vm.host_name = "compute1"
    instance.vm.network "private_network", ip: "10.0.0.31", netmask: "255.255.255.0"
    instance.vm.network "private_network", ip: "192.168.50.31", netmask: "255.255.255.0"
    instance.vm.provider "virtualbox" do |vb|
      vb.memory = "4096"
      vb.cpus = 4
      vb.customize ["modifyvm", :id, "--natdnshostresolver1", "on"]
    end
    instance.vm.provision "shell", inline: <<-SHELL
        echo "10.0.0.11 controller" | sudo tee -a /etc/hosts
        echo "10.0.0.31 compute1" | sudo tee -a /etc/hosts
        echo "10.0.0.41 storage1" | sudo tee -a /etc/hosts
    SHELL
  end

  config.vm.define "storage1" do |instance|
    instance.vm.box = "centos/7"
    instance.vm.host_name = "storage1"
    instance.vm.network "private_network", ip: "10.0.0.41", netmask: "255.255.255.0"
    instance.vm.provider "virtualbox" do |vb|
      vb.memory = "1536"
      vb.cpus = 2
      vb.customize ["modifyvm", :id, "--natdnshostresolver1", "on"]
      unless File.exist?(storage_disk)
        vb.customize ['createhd', '--filename', storage_disk, '--size', 6 * 1024]
      end
      vb.customize ['storageattach', :id, '--storagectl', 'IDE Controller', '--port', 1, '--device', 0, '--type', 'hdd', '--medium', storage_disk]
    end
    instance.vm.provision "shell", inline: <<-SHELL
        echo "10.0.0.11 controller" | sudo tee -a /etc/hosts
        echo "10.0.0.31 compute1" | sudo tee -a /etc/hosts
        echo "10.0.0.41 storage1" | sudo tee -a /etc/hosts
    SHELL
  end
end

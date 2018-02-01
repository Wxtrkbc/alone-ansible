# -*- mode: ruby -*-
# vi: set ft=ruby :
Vagrant.configure("2") do |config|
    config.vm.define "postgres" do |postgres|
        postgres.vm.box = "ubuntu/trusty64"
        postgres.vm.network "private_network", ip: "192.168.33.9"
        postgres.vm.provider "virtualbox" do |v|
            v.memory = 1024
        end
    end
    config.vm.define "web" do |web|
        web.vm.box = "ubuntu/trusty64"
        web.vm.network "private_network", ip: "192.168.33.10"
        web.vm.provider "virtualbox" do |v|
            v.memory = 1024
        end
    end
    config.vm.define "elk" do |elk|
        elk.vm.box = "ubuntu/trusty64"
        elk.vm.network "private_network", ip: "192.168.33.11"
        elk.vm.provider "virtualbox" do |v|
            v.memory = 2048
        end
    end
    config.vm.define "nginx" do |nginx|
        nginx.vm.box = "ubuntu/trusty64"
        nginx.vm.network "private_network", ip: "192.168.33.12"
        nginx.vm.provider "virtualbox" do |v|
            v.memory = 1024
        end
    end
end
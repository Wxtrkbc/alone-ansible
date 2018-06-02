# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
  # Base VM OS configuration.
  config.vm.box = "ubuntu/xenial64"
  config.ssh.insert_key = false

  config.vm.provider :virtualbox do |v|
    v.memory = 256
    v.cpus = 1
    v.linked_clone = true
  end

  # Define  VMs with static private IP addresses.
  boxes = [
    { :name => "bal1", :ip => "192.168.4.1" },
    { :name => "bal2", :ip => "192.168.4.2" },
    { :name => "app1", :ip => "192.168.4.3" },
    { :name => "app2", :ip => "192.168.4.4" },
    { :name => "db1", :ip => "192.168.4.5" },
    { :name => "db2", :ip => "192.168.4.6" },
    { :name => "redis", :ip => "192.168.4.7" },
    { :name => "sentry", :ip => "192.168.4.8" },
    { :name => "elk", :ip => "192.168.4.9" },
  ]

  # Provision each of the VMs.
  boxes.each do |opts|
    config.vm.define opts[:name] do |config|
      config.vm.hostname = opts[:name]
      config.vm.network :private_network, ip: opts[:ip]
    end
  end

end

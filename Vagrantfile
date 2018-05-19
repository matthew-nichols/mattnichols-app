# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
  # this is just a single ubuntu box for now, like production
  config.vm.box = "ubuntu/xenial64"

  # for ansible we will use the insecure key to make life easier
  # (security isn't needed for testing)
  config.ssh.insert_key = false

  config.vm.network "private_network", ip: "192.168.33.10"
end

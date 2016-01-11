# -*- mode: ruby -*-
# vi: set ft=ruby :

VAGRANTFILE_API_VERSION = "2"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|

  config.vm.define "monitor" do |monitor|
    monitor.vm.box = "ubuntu/trusty64"
    monitor.vm.hostname = "monitor.dev"
    monitor.vm.network :private_network, ip: "192.168.30.33"
    monitor.ssh.insert_key = false
  end

  config.vm.provider "virtualbox" do |v|
    v.customize [
        "modifyvm", :id,
        "--name", "monitor-error-server",
        "--memory", "2048"
        ]
  end

end




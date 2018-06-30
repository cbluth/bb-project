# -*- mode: ruby -*-
# vi: set ft=ruby :

VAGRANT_API_VERSION = 2



Vagrant.configure(VAGRANT_API_VERSION) do |config|
  config.ssh.insert_key = false
  config.vm.synced_folder '.', '/vagrant', disabled: true
  config.vm.provision 'shell', inline: <<-SHELL
    sudo ln -s /usr/bin/python3 /usr/bin/python;
    sudo pkill apt || true
  SHELL

  config.vm.define 'minikube' do |minikube|
    minikube.vm.hostname = 'minikube'
    minikube.vm.box = 'ubuntu/bionic64'
    minikube.vm.network "private_network", ip: "192.168.56.11"
  end

  config.vm.provider "virtualbox" do |minikube|
    minikube.memory = 4096
    minikube.cpus = 2
  end
end

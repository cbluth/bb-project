# -*- mode: ruby -*-
# vi: set ft=ruby :

VAGRANT_API_VERSION = 2

Vagrant.configure(VAGRANT_API_VERSION) do |config|
  config.ssh.insert_key = false
  config.vm.provision 'shell', inline: <<-SHELL
    sudo ln -s /usr/bin/python3 /usr/bin/python;
    sudo systemctl stop apt-daily.timer;
    sudo systemctl disable apt-daily.timer;
    sudo pkill apt
  SHELL

  config.vm.define 'minikube' do |el1|
    el1.vm.hostname = 'minikube'
    el1.vm.box = 'ubuntu/bionic64'
    el1.vm.network "private_network", ip: "192.168.56.11"
  end
end

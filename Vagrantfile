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

  config.vm.define 'kube' do |kube|
    kube.vm.hostname = 'kube'
    kube.vm.box = 'ubuntu/bionic64'
    kube.vm.network "private_network", ip: "192.168.56.11"
  end

  config.vm.provider "virtualbox" do |kube|
    kube.memory = 4096
    kube.cpus = 2
  end

  config.vm.provision "ansible" do |ansible|
    ansible.playbook = "ansible/site.yml"
  end

end

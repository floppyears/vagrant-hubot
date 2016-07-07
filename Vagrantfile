# -*- mode: ruby -*-
# vi: set ft=ruby sw=2 noet :

# Vagrantfile API/syntax version. Don't touch unless you know what you're doing!
VAGRANTFILE_API_VERSION = "2"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|
  config.vm.define('hubot')

  config.vm.box = "centos-6.7"
  config.vm.box_url = "https://github.com/CommanderK5/packer-centos-template/releases/download/0.6.7/vagrant-centos-6.7.box"

  # config.vm.network :forwarded_port, guest: 8080, host: 8080
  config.vm.network :private_network, ip: "192.168.33.12"

  config.vm.provision :ansible do |ansible|
    ansible.playbook = 'playbook.yaml'
  end
end

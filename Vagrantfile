# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
  config.vm.box = "ubuntu/xenial64"
  config.vm.network "private_network", ip: "10.0.0.10"
  config.vm.provision "ansible_local" do |ans|
    ans.playbook = "nginx.yaml"
	ans.install = true
	ans.install_mode = "pip"
	ans.pip_install_cmd = "curl https://bootstrap.pypa.io/pip/3.5/get-pip.py | sudo python"
  end
end
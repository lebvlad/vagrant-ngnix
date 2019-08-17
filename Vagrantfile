# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
  config.vm.box = "ubuntu/bionic64"
  config.vm.network "forwarded_port", guest: 80, host: 8080
  config.vm.network "public_network"
  config.vm.provision "shell", path: ".provision/ubuntu_update.sh", run: 'always'
  config.vm.provision "shell", path: ".provision/ngnix_install.sh"
end

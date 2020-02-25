# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
    config.vm.define "web1" do |web1|
        web1.vm.box = "ubuntu/xenial64"
	web1.vm.network "forwarded_port", guest: 80, host:8080
	web1.vm.synced_folder "www_1", "/var/www/html"
	web1.vm.provision "shell", path: "script.sh"
    end
    config.vm.define "web2" do |web2|
        web2.vm.box = "ubuntu/xenial64"
	web2.vm.network "forwarded_port", guest:80, host:8008
	web2.vm.synced_folder "www_2", "/var/www/html"
	web2.vm.provision "shell", path: "script.sh"
    end
  end
  
  

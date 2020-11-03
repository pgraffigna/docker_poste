# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
  config.ssh.insert_key = false
  config.vm.synced_folder ".", "/vagrant", disabled: true
  
  config.vm.define "poste" do |p|
    p.vm.box = "geerlingguy/ubuntu2004"
    p.vm.network "private_network", ip: "192.168.60.10"
    p.vm.hostname = "poste"
    p.vm.network "forwarded_port", guest: 443, host: 4443
    p.vm.provision :docker
    p.vm.provision :docker_compose	

    p.vm.provider :virtualbox do |vb|
      vb.customize ["modifyvm", :id, "--memory", "1024"]
      vb.customize ["modifyvm", :id, "--cpus", "1"]
    end 
  end  
end

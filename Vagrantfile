# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
  config.vm.synced_folder ".", "/vagrant", disabled: true
#  config.ssh.password = "vagrant"
  config.disksize.size = "20GB"
#  config.vm.provision "shell", inline: <<-SHELL
#    set -e -x -u
#    sed -i 's/PasswordAuthentication no/PasswordAuthentication yes/g' /etc/ssh/sshd_config
#    # Restart sshd
#    systemctl restart sshd.service
#  SHELL
  config.vm.define "master1" do |master1|
    master1.vm.box = "centos/8"

    master1.vm.network "private_network", ip: "192.168.33.10"
    master1.vm.hostname = "master1"
  

    master1.vm.provider "virtualbox" do |vb|
  #   # Display the VirtualBox GUI when booting the machine
      vb.gui = false
      vb.memory = "4096"
      vb.cpus  = "2"
      vb.name = "master1"
    end
  end
  
  config.vm.define "master2" do |master2|
    master2.vm.box = "centos/8"

  

    master2.vm.network "private_network", ip: "192.168.33.11"
    master2.vm.hostname = "master2"
    master2.vm.provider "virtualbox" do |vb|
  #   # Display the VirtualBox GUI when booting the machine
      vb.gui = false
      vb.memory = "4096"
      vb.cpus  = "2"
      vb.name = "master2"
    end
  end
  config.vm.define "master3" do |master3|
    master3.vm.box = "centos/8"

    master3.vm.network "private_network", ip: "192.168.33.12"
    master3.vm.hostname = "master3"
  

    master3.vm.provider "virtualbox" do |vb|
  #   # Display the VirtualBox GUI when booting the machine
      vb.gui = false
      vb.memory = "4096"
      vb.cpus  = "2"
      vb.name = "master3"
    end
  end
  config.vm.define "worker1" do |worker1|
    worker1.vm.box = "centos/8"

    worker1.vm.network "private_network", ip: "192.168.33.13"
    worker1.vm.hostname = "worker1"

    worker1.vm.provider "virtualbox" do |vb|
  #   # Display the VirtualBox GUI when booting the machine
      vb.gui = false
      vb.memory = "8192"
      vb.cpus  = "2"
      vb.name = "worker1"
    end
  end

  config.vm.define "worker2" do |worker2|
    worker2.vm.box = "centos/8"

    worker2.vm.network "private_network", ip: "192.168.33.14"
    worker2.vm.hostname = "worker2"
  

    worker2.vm.provider "virtualbox" do |vb|
  #   # Display the VirtualBox GUI when booting the machine
      vb.gui = false
      vb.memory = "8192"
      vb.cpus  = "2"
      vb.name = "worker2"
    end
  end

  config.vm.define "worker3" do |worker3|
    worker3.vm.box = "centos/8"

    worker3.vm.network "private_network", ip: "192.168.33.15"
    worker3.vm.hostname = "worker3"
  # config.vm.network "public_network" 

  # config.vm.synced_folder "../data", "/vagrant_data"

    worker3.vm.provider "virtualbox" do |vb|
  #   # Display the VirtualBox GUI when booting the machine
      vb.gui = false
      vb.memory = "8192"
      vb.cpus  = "2"
      vb.name = "worker3"
    end
  end
end 

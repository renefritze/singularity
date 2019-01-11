# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
  config.vm.box = "sylabs/singularity-3.0-ubuntu-bionic64"
  config.vm.box_version = "20190108.0.0"

  # Enable provisioning with a shell script. Additional provisioners such as
  # Puppet, Chef, Ansible, Salt, and Docker are also available. Please see the
  # documentation for more information about their specific syntax and use.
  config.vm.provision "shell", inline: <<-SHELL
    apt-get update
    apt-get install -y git
    singularity build -F pymor-demo.sif /vagrant/Singularity.master
  SHELL
end

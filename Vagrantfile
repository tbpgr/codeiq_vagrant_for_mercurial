# -*- mode: ruby -*-
# vi: set ft=ruby :

$script = <<SCRIPT
apt-get update -y
apt-get install -y mercurial
SCRIPT

VAGRANTFILE_API_VERSION = "2"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|
  config.vm.box = "precise32"
  config.vm.box_url = 'http://files.vagrantup.com/'+config.vm.box+'.box'

  config.vm.provision "shell", inline: "echo 'start provision'"
  config.vm.provision "shell", inline: $script
  config.vm.provision "shell", inline: "echo 'finish provision'"
end

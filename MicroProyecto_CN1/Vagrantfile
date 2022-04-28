# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|

  if Vagrant.has_plugin? "vagrant-vbguest"
    config.vbguest.no_install  = true
    config.vbguest.auto_update = false
    config.vbguest.no_remote   = true
  end

#  config.vm.define :clienteUbuntu do |clienteUbuntu|
#    clienteUbuntu.vm.box = "bento/ubuntu-20.04"
#    clienteUbuntu.vm.network :private_network, ip: "192.168.100.2"
#    clienteUbuntu.vm.hostname = "clienteUbuntu"
#  end

#  config.vm.define :servidorUbuntu do |servidorUbuntu|
#    servidorUbuntu.vm.box = "bento/ubuntu-20.04"
#    servidorUbuntu.vm.network :private_network, ip: "192.168.100.3"
#    servidorUbuntu.vm.provision "shell", path: "script.sh"
#    servidorUbuntu.vm.hostname = "servidorUbuntu"
#  end

  config.vm.define :proxyServer do |proxyServer|
    proxyServer.vm.box = "bento/ubuntu-20.04"
    proxyServer.vm.network :private_network, ip: "192.168.100.22"
    proxyServer.vm.provision "shell", path: "Scripts/Script_proxy.sh"
    proxyServer.vm.hostname = "proxyServer"
  end

  config.vm.define :servidorU1 do |servidorU1|
    servidorU1.vm.box = "bento/ubuntu-20.04"
    servidorU1.vm.network :private_network, ip: "192.168.100.4"
    servidorU1.vm.provision "shell", path: "Scripts/Script_serverU1.sh"
    servidorU1.vm.hostname = "servidorU1"
  end

  config.vm.define :servidorU2 do |servidorU2|
    servidorU2.vm.box = "bento/ubuntu-20.04"
    servidorU2.vm.network :private_network, ip: "192.168.100.5"
    servidorU2.vm.provision "shell", path: "Scripts/Script_serverU2.sh"
    servidorU2.vm.hostname = "servidorU2"
  end

# $install_puppet = <<-PUPPET
# sudo apt-get update -y
# sudo apt-get install -y puppet
# PUPPET

#  config.vm.box = "bento/ubuntu-20.04"
#  config.vm.hostname = "puppetServer"
#  config.vm.network :private_network, ip: "192.168.90.3"
#  config.vm.provision "shell", inline: $install_puppet
#  config.vm.provision :puppet do |puppet|
#    puppet.manifests_path = "puppet/manifest"
#    puppet.manifest_file = "site.pp"
#    puppet.module_path = "puppet/modules" 
#  end

end





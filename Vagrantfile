# -*- mode: ruby -*-
# vi: set ft=ruby :
load "settings.sh"

Vagrant.configure("2") do |config|
  #Configurando o SO
  config.vm.box = VB_IMAGE
    
  #Configurando para modo autônomo onde o servidor LTSP fornece serviços DHCP aos clientes	
  if STANDALONE.downcase == "yes"		
    config.vm.network "public_network", ip: LAN_IP, netmask: "255.255.255.0", bridge: LAN_IF
  #Configurando modo normal onde existe um servidor DHCP na LAN que fornece o serviço DHCP aos clientes
  else
    config.vm.network "public_network", auto_config: true, bridge: LAN_IF
  end
  
  config.vm.provider "virtualbox" do |virtualbox|
	  # Enable promiscuous mode
  	  virtualbox.customize ["modifyvm", :id, "--nicpromisc2", "allow-all"]
  	  virtualbox.memory = VB_RAM
   end
  #Configurando a máquina virtual
  config.vm.provider "virtualbox" do |vb|
    vb.gui = true
    vb.memory = "1024"
   end

  config.vm.synced_folder ".", "/vagrant"
  

end

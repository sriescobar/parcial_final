Vagrant.configure("2") do |config|
	if Vagrant.has_plugin?("vagrant-vbguest")
		config.vbguest.auto_update = false 
	 end
	config.vm.define :firewall do |firewall|
	 firewall.vm.box = "bento/centos-7"
	 firewall.vm.network :public_network, ip: "192.168.10.2"
	 firewall.vm.network :private_network, ip: "192.168.50.2"
	 firewall.vm.hostname = "firewall"
	 firewall.vm.provision "shell", path: "./firewallscript.sh"
	end
	config.vm.define :servidorSTRM do |servidorSTRM|
	 servidorSTRM.vm.box = "bento/centos-7"
	 servidorSTRM.vm.network :private_network, ip: "192.168.50.3"
	 servidorSTRM.vm.hostname = "servidorSTRM"
	 servidorSTRM.vm.provision "shell", path: "./servidorSTRM.sh"
	 
     
	 end
	end
	
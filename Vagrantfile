Vagrant.configure("2") do |config|

  config.vm.box = "generic/ubuntu2004"
  config.vm.hostname = "ubuntu-test"
  
  config.vm.network :private_network, ip: "192.168.56.20"
  config.vm.network "forwarded_port", 
    guest: 3000, host: 3000, 
    protocol: "tcp"

  config.vm.provision "file", 
    source: "services",
    destination: "$HOME/services"
  
  config.vm.provision "ansible" do |ansible|
    ansible.playbook = "ansible/install.yml"
  end 

end

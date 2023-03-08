Vagrant.configure("2") do |config|
  config.vm.box = "ubuntu/focal64"
  config.vm.network "public_network"
  config.vm.network "forwarded_port", guest: 80, host: 5555
 
  config.vm.provider "virtualbox" do |vb|
  vb.name = "desafio01"  
  vb.memory = "1024"
  vb.cpus = "2"
  end
  config.vm.provision "shell", inline: <<-SHELL
  apt-get update
  apt-get install -y nginx
  apt-get install -y net-tools
  apt-get install -y nmap
  apt-get install -y telnet
  apt-get install -y htop
  apt-get install -y wget
  apt-get install -y unzip
  apt-get install -y curl
  SHELL
end

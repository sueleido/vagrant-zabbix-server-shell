Vagrant.configure("2") do |config|
    config.vm.box = "ubuntu/focal64"
    config.vm.network "public_network"
    config.vm.provider "virtualbox" do |vb|
      vb.memory = "2048"
      vb.cpus = "2"
      vb.name = "vagrant-zabbix-serverr"
    end
  
    config.vm.boot_timeout = 1000 
    config.vm.provision "file", source: "comand1.sql", destination: "/home/vagrant/comand1.sql.sql"
    config.vm.provision "file", source: "comand2.sql", destination: "/home/vagrant/comand2.sql.sql"
    config.vm.provision "shell", path: "config-serv-ubuntu.sh"
  end
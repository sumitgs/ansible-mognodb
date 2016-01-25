Vagrant.configure(2) do |config|
  config.vm.box = "hashicorp/precise64"
  config.ssh.insert_key = false

  config.vm.define "mon1" do |server|
    server.vm.network "private_network", ip: "10.0.0.103"
    server.vm.network "forwarded_port", guest: 27017, host: 20017
    server.vm.hostname = "mon-1"
  end

  config.vm.define "mon2" do |server|
    server.vm.network "private_network", ip: "10.0.0.104"
    server.vm.network "forwarded_port", guest: 27017, host: 21017
    server.vm.hostname = "mon-2"
  end

  config.vm.define "mon3" do |server|
    server.vm.network "private_network", ip: "10.0.0.105"
    server.vm.network "forwarded_port", guest: 27017, host: 22017
    server.vm.hostname = "mon-3"
  end


  config.vm.provider "virtualbox" do |v|
    v.gui = false
    memory = "1024"
  end
end
Vagrant.configure(2) do |config|
  config.vm.box = "hashicorp/precise64"
  config.ssh.insert_key = false

  config.vm.define "mongo1" do |server|
    server.vm.network "private_network", ip: "10.0.0.103"
    server.vm.hostname = "mongo2"
  end

  config.vm.define "mongo2" do |server|
    server.vm.network "private_network", ip: "10.0.0.104"
    server.vm.hostname = "mongo3"
  end

  config.vm.define "mongo3" do |server|
    server.vm.network "private_network", ip: "10.0.0.105"
    server.vm.hostname = "mongo4"
  end


  config.vm.provider "virtualbox" do |v|
    v.gui = false
    memory = "1024"
  end
end
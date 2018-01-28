Vagrant.configure("2") do |config|

######################### ansible-caddy node
  config.vm.define "caddy" do |caddy|
    caddy.vm.box = "geerlingguy/centos7"
    caddy.vm.hostname = "caddy"
    caddy.vm.network :private_network, ip: "192.168.56.100"
  end

##################### Setting CPU and Memory for All machines
  config.vm.provider "virtualbox" do |vb|
    vb.gui = false
    vb.memory = "512"
    vb.cpus =  1
  end

####################### Sharing Folder with machines
  config.vm.synced_folder ".", "/home/vagrant/projects", type: "nfs"
  config.ssh.insert_key = false
end

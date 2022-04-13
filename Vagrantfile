Vagrant.configure("2") do |config|
  config.vm.define "open5gs-compose"

  config.vm.provider "virtualbox" do |vb|
    vb.memory = 16384
    vb.cpus = 16
  end

  config.vm.hostname = "open5gs"
  config.vm.box = "ubuntu/bionic64"
  config.ssh.forward_agent = true
  config.vm.network "forwarded_port", guest: 3000, host: 5000
  config.vm.synced_folder "shared", "/vagrant", disabled: false
  
  config.vm.provision "shell", path: "pre-config.sh"
  config.vm.provision :reload
  config.vm.provision "shell", path: "post-config.sh"

end

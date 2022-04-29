Vagrant.configure("2") do |config|
  config.vm.box = "generic/ubuntu2004"
  config.vm.define "ubuntu"
  config.vm.provider "virtualbox" do |vbox|
    vbox.name = "ubuntu"
    vbox.memory = "4096"
    vbox.cpus = 2
  end

  config.vm.hostname = "ubuntu"

      
  config.vm.network "private_network", ip: "192.168.56.100"
  config.vm.network "forwarded_port", guest: 3000, host: 3000
  config.vm.network "forwarded_port", guest: 9090, host: 9090

  config.vm.provision :ansible do |ansible|
      ansible.playbook = "ansible/main.yml"
  end

end

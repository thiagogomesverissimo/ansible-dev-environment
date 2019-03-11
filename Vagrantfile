VAGRANTFILE_API_VERSION = "2"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|

  config.vm.define "debian" do |host| 
    host.vm.box = "debian/stretch64"
    host.vm.network :private_network, ip: "192.168.77.41"
    config.ssh.insert_key = false # important

    host.vm.provider :virtualbox do |v|
      v.name = "debian"
      v.memory = 1024
      v.cpus = 1
      v.customize ["modifyvm", :id, "--natdnshostresolver1", "on"]
      v.customize ["modifyvm", :id, "--ioapic", "on"]
      v.customize ["modifyvm", :id, "--natdnsproxy1", "on"]
      v.customize ["modifyvm", :id, "--groups", "/network77"]
    end
  end

  config.vm.define "ubuntu" do |host| 
    host.vm.box = "bento/ubuntu-18.04"
    host.vm.network :private_network, ip: "192.168.77.42"
    config.ssh.insert_key = false # important

    host.vm.provider :virtualbox do |v|
      v.name = "ubuntu"
      v.memory = 1024
      v.cpus = 1
      v.customize ["modifyvm", :id, "--natdnshostresolver1", "on"]
      v.customize ["modifyvm", :id, "--ioapic", "on"]
      v.customize ["modifyvm", :id, "--natdnsproxy1", "on"]
      v.customize ["modifyvm", :id, "--groups", "/network77"]
    end
  end

end

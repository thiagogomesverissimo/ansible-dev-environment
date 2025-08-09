VAGRANTFILE_API_VERSION = "2"
ENV['VAGRANT_DEFAULT_PROVIDER'] = 'libvirt'

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|

    ### global configs
    config.ssh.insert_key = false # important

    ## Modelo antigo com virtualbox
    #config.vm.define "debian" do |host| 
    #  host.vm.box = "debian/stretch64"
    #  host.vm.network :private_network, ip: "192.168.77.41"
    #  config.ssh.insert_key = false # important

    #  host.vm.provider :virtualbox do |v|
    #    v.name = "debian"
    #    v.memory = 1024
    #    v.cpus = 1
    #    v.customize ["modifyvm", :id, "--natdnshostresolver1", "on"]
    #    v.customize ["modifyvm", :id, "--ioapic", "on"]
    #    v.customize ["modifyvm", :id, "--natdnsproxy1", "on"]
    #    v.customize ["modifyvm", :id, "--groups", "/network77"]
    #  end
    #end

    # 192.168.7.2
    config.vm.define "debian11" do |host|
      host.vm.hostname = "debian11"
      host.vm.box = "generic/debian11"
      host.vm.network :private_network,
        :ip => "192.168.7.2",
        :libvirt__network_name => "devenv",
        :libvirt__forward_mode => "nat"
      host.vm.provider :libvirt do |v|
        v.memory = 2048
        v.cpus = 2
      end
    end

    # 192.168.7.3
    config.vm.define "debian12" do |host|
      host.vm.hostname = "debian12"
      host.vm.box = "debian/bookworm64"
      host.vm.network :private_network,
        :ip => "192.168.7.3",
        :libvirt__network_name => "devenv",
        :libvirt__forward_mode => "nat"
      host.vm.provider :libvirt do |v|
        v.memory = 2048
        v.cpus = 2
      end
    end

    # 192.168.7.4
    # 192.168.7.5
    # 192.168.7.6
    # 192.168.7.7
    # 192.168.7.8
    # 192.168.7.9
    # 192.168.7.10

  
end

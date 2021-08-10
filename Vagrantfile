Vagrant.configure("2") do |config|
    config.vm.define "cent7" do |machine|
        
        machine.vm.box = "centos/7"
        machine.ssh.insert_key = false
        machine.vm.hostname = "cent7"

        config.vm.provider "virtualbox" do |vb|
            # v.customize ["modifyvm", :id, "--cpuexecutioncap", "50"]
            vb.name = "vagrant_cent7"
            vb.memory = 1024  
            vb.cpus = 1
    end
    
    config.vm.network "private_network", ip: "192.168.56.151" #, :name => 'VirtualBox Host-Only Ethernet Adapter', :adapter => 2
 
    config.vm.synced_folder '.', '/vagrant', type: 'rsync', disabled: true
    config.vm.synced_folder '.', '/vagrant', disabled: true

    end
end

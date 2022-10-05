
Vagrant.configure("2") do |config|

  config.vm.box_check_update = false

  # Creates NFS VM
  config.vm.define "nfs" do |nfs|
    nfs.vm.box = "ubuntu/focal64"
    # Create a private network, which allows host-only access to the machine using a specific IP.
    nfs.vm.network "public_network", ip: "192.168.10.20", bridge: "enp6s0"
    nfs.vm.network "private_network", ip: "10.0.0.1"

    # Customize the amount of memory and cpu on the VM:
    nfs.vm.provider "virtualbox" do |vb|
      vb.gui = false
      vb.name = "nfs"
      vb.memory = 512
      vb.cpus = 1  
    end
  end

# -----------------------------------------------------------------------------------------------------
  # Creates Emby VM
  config.vm.define "emby" do |emby|
    emby.vm.box = "ubuntu/focal64"
    # Create a private network, which allows host-only access to the machine using a specific IP.
    emby.vm.network "public_network", ip: "192.168.10.21", bridge: "enp6s0"
    emby.vm.network "private_network", ip: "10.0.0.2"
    # Customize the amount of memory and cpu on the VM:
    emby.vm.provider "virtualbox" do |vb|
      vb.gui = false
      vb.name = "emby"
      vb.memory = 512
      vb.cpus = 1
    end
  end

  # Creates transmission VM
  config.vm.define "transmission" do |tsm|
    tsm.vm.box = "ubuntu/focal64"
    # Create a private network, which allows host-only access to the machine using a specific IP.
    tsm.vm.network "public_network", ip: "192.168.10.22", bridge: "enp6s0"
    tsm.vm.network "private_network", ip: "10.0.0.3"

    # Customize the amount of memory and cpu on the VM:
    tsm.vm.provider "virtualbox" do |vb|
      vb.gui = false
      vb.name = "transmission"
      vb.memory = 512
      vb.cpus = 1
    end
  end

end


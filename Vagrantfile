Vagrant.configure("2") do |config|

  config.vm.box = "debian/bookworm64"

  config.vm.hostname = "pj9f4a12-jagahi.clotjfe.net"

  config.vm.network "public_network"

  config.vm.provider "virtualbox" do |vb|
    vb.memory = 2048
    vb.cpus   = 3
  end

  config.vm.provision "shell", inline: <<-SHELL
    apt update
    apt install -y net-tools whois docker.io
    usermod -aG docker vagrant
  SHELL

end
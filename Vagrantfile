Vagrant.configure("2") do |config|
  (1..3).each do |i|
    config.vm.define "server#{i}" do |server|
      server.vm.box = "ubuntu/bionic64"
      server.vm.hostname = "server#{i}"
      server.vm.network "private_network", ip: "192.168.56.#{100 + i}"
      server.vm.provider "virtualbox" do |vb|
        vb.memory = "256"
        vb.cpus = 1
      end
    end
  end
end

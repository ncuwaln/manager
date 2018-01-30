$node1 = "192.168.0.121"
$node2 = "192.168.0.122"
$node3 = "192.168.0.123"


Vagrant.configure("2") do |config|

  config.vm.define "node1" do |node1|
    node1.vm.hostname="node1"
    node1.vm.box = "CentOS7"
    node1.ssh.password = "vagrant"
    node1.vm.network "public_network", ip: $node1, bridge: "wlp3s0"
    node1.vm.provision :shell, inline: "echo 'root:root' | sudo chpasswd"
    node1.vm.synced_folder ".", "/vagrant", type: "rsync"
  end

  config.vm.define "node2" do |node2|
    node2.vm.hostname="node2"
    node2.vm.box = "CentOS7"
    node2.ssh.password = "vagrant"
    node2.vm.network "public_network", ip: $node2, bridge: "wlp3s0"
    node2.vm.provision :shell, inline: "echo 'root:root' | sudo chpasswd"
    node2.vm.synced_folder ".", "/vagrant", type: "rsync"
  end

  config.vm.define "node3" do |node3|
    node3.vm.hostname="node3"
    node3.vm.box = "CentOS7"
    node3.ssh.password = "vagrant"
    node3.vm.network "public_network", ip: $node3, bridge: "wlp3s0"
    node3.vm.provision :shell, inline: "echo 'root:root' | sudo chpasswd"
    node3.vm.synced_folder ".", "/vagrant", type: "rsync"
  end
end

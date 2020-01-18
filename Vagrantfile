Vagrant.configure("2") do |config|

  config.vm.box = "generic/ubuntu1904"

  config.vm.provider "virtualbox" do |vb|
    vb.memory = "1024"
  end

  config.vm.define "wordpress" do |m|
    m.vm.network "private_network", ip: "172.17.177.43"
  end

  config.vm.define "mysql" do |m|
    m.vm.network "private_network", ip: "172.17.177.44"
  end

end

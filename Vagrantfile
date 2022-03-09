Vagrant.configure("2") do |config|

  config.vm.box = "ubuntu/bionic64"
  config.vm.box_download_insecure = true

  config.vm.define "kub01" do |kub01|
      kub01.vm.network "private_network", ip: "192.168.56.10"
      kub01.vm.synced_folder "share/", "/share"

      kub01.vm.provider "virtualbox" do |vb|
        vb.memory = 1024
        vb.cpus = 2
        vb.name = "kub01"
      end
  end
end
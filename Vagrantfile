Vagrant.configure("2") do |config|
  config.vm.box = "ubuntu1404x64"
  config.vm.box_url = "https://cloud-images.ubuntu.com/vagrant/trusty/current/trusty-server-cloudimg-amd64-vagrant-disk1.box"
  config.vm.network "private_network", ip: "192.168.50.4"
  config.vm.provision :shell, path: "bootstrap.sh"
  config.vm.synced_folder "./web/", "/vagrant/web", id: "123", group: 'www-data', owner: 'www-data', mount_options: ["dmode=775", "fmode=764"]
end
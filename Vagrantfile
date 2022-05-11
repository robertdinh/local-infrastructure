Vagrant.configure("2") do |config|
    config.vm.box = "bento/ubuntu-20.04"
    config.vm.network "forwarded_port", host: 8000, guest: 8000
    config.vm.network "forwarded_port", host: 3306, guest: 3306
    config.vm.synced_folder ".", "/home/vagrant/workspace", type: "virtualbox", disabled: false
    config.vm.disk :disk, size: "100GB", primary: true
    config.vm.provider 'virtualbox' do |v|
      v.memory = 4096
      v.cpus = 2
    end
end
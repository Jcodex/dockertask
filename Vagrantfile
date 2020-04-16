Vagrant.configure("2") do |config|
config.vm.define "my-virtual-machine2"
config.vm.synced_folder '.', '/vagrant', disabled: true
config.vm.box = "hashicorp/bionic64"
config.vm.network :forwarded_port, host: 8000, guest: 8000
config.vm.network :forwarded_port, host: 8080, guest: 80
# config.vm.network "public_network"
config.vm.provision "ansible" do |ansible|
ansible.verbose = "v"
ansible.playbook = "playbook.yml"
end
end

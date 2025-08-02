Vagrant.configure("2") do |config|
  config.vm.box = "ubuntu/bionic64"

  config.vm.network "private_network", type: "dhcp"

  config.vm.synced_folder ".", "/vagrant"

  config.vm.provision "ansible_local" do |ansible| #ansible_local utiliza la instalacion local y ansible utiliza la de un externo, como wsl
    ansible.playbook = "playbook.yml"
 
  end
end

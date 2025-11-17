Vagrant.configure(2) do |config|
  config.vm.define "HW18host" do |node|
    node.vm.box = "boxen/ubuntu-24.04"
    #node.vm.synced_folder ".", "/vagrant"
    node.vm.synced_folder ".", "/vagrant", disabled: true
    node.vm.hostname = "HW18host"
      node.vm.provider "virtualbox" do |vb|
        vb.memory = "1024"
        vb.name = "HW18host"
        vb.cpus = 1
      end
  end
  config.vm.provision "ansible" do |ansible|
    ansible.playbook = "dscode.yml"
  end
end

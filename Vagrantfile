Vagrant.configure("2") do |config|

  config.vm.box = "ubuntu/bionic64"
  config.vm.define "ubuntuvagrant"
  config.vm.hostname = "ubuntuvagrant.local"
  config.vm.network "public_network", auto_config: true

  #
  # Run Ansible from the Vagrant Host
  #
  config.vm.provision "ansible" do |ansible|
   ansible.playbook = "provisioning/playbook.yml"
   ansible.groups = {
     "ubuntuvagrant" => ["ubuntuvagrant"]
   }
  end

end

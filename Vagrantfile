Vagrant.configure("2") do |config|

  config.vm.box = "bento/ubuntu-18.04"
  config.vm.define "ubuntuvagrant"
  config.vm.hostname = "ubuntuvagrant.local"
  # was added to make vm accessible to other machine on the same network, it use another address on the network port that gonna be selected
  config.vm.network "public_network", auto_config: true

  #
  # Run Ansible from the Vagrant Host
  #
#  config.vm.provision "ansible" do |ansible|
#   ansible.playbook = "provisioning/playbook.yml"
#   ansible.groups = {
#     "ubuntuvagrant" => ["ubuntuvagrant"]
#   }
#  end

  # this block was added to enable remote ssh using password
  config.vm.provision "shell" do |s|
    s.inline = "sed -i.bak 's/^#*\s*PasswordAuthentication.*/PasswordAuthentication yes/g' /etc/ssh/sshd_config"
  end
end

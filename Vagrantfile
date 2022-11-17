Vagrant.configure(2) do |config|

  # Disable the new default behavior introduced in Vagrant 1.7, to
  # ensure that all Vagrant machines will use the same SSH key pair.
  # See https://github.com/mitchellh/vagrant/issues/5005
  config.ssh.insert_key = false
  config.vm.box = "ubuntu/bionic64"
  config.vm.network "private_network", :ip => "10.2.2.70"

  config.vm.provision "ansible" do |ansible|
    ansible.playbook = "playbook.yml"
  end
end

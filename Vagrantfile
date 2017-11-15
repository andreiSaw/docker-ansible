Vagrant.configure("2") do |config|
  # The most common configuration options are documented and commented below.
  # For a complete reference, please see the online documentation at
  # https://docs.vagrantup.com.

  # Every Vagrant development environment requires a box. You can search for
  # boxes at https://vagrantcloud.com/search.
  config.vm.box = "ubuntu/trusty64"
  config.ssh.insert_key = false
config.vm.provision "ansible" do |ansible|
  ansible.verbose = "v"
  ansible.playbook = "main.yml"
  ansible.groups = {
     'localhost' => ['default']
   }
  end
end

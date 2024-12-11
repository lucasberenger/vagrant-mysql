Vagrant.configure("2") do |config|
 config.vm.box = "bento/ubuntu-22.04"
 config.vm.network "forwarded_port", guest: 80, host: 8090
 config.vm.network "public_network"
 config.vm.provision "shell",
  path: "script.sh"
 config.vm.synced_folder "site/", "/var/www/html"
 
 config.vm.provision "ansible" do |ansible|
  ansible.playbook = "playbook.yml"
 end
end

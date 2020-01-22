$msg = <<MSG
----------------------------------------------------------
The machine is up and running. Visit the application here:

  http://localhost:4000

Existing user accounts:

  admin:Admin_123
  user1:User1_123
  user2:User2_123
----------------------------------------------------------
MSG

Vagrant.configure("2") do |nodegoat|
  nodegoat.vm.post_up_message = $msg
  nodegoat.vm.box = "ubuntu/bionic64"
  nodegoat.vm.network "forwarded_port", guest: 4000, host: 4000
  nodegoat.vm.provision "ansible" do |ansible|
    ansible.playbook = "nodegoat.yml"
    ansible.compatibility_mode = "2.0"
  end
end

Vagrant.configure("2") do |config|
    config.vm.box = 'focal-server-box'
    config.vm.box_version = '20210304'
    config.vm.box_url = 'metadata.json'
    
    config.vm.provider :virtualbox do |v| 
        v.customize ["modifyvm", :id, "--memory", 1024]
    end

    config.vm.provision "ansible" do |ansible|
        ansible.playbook = "playbook.yml"
     #   ansible.inventory_path = ".vagrant/provisioners/ansible/inventory/vagrant_ansible_inventory"
    end
        
end
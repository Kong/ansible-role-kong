# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure(2) do |config|
    config.vm.box = "ubuntu/trusty64"

    config.vm.provision "ansible" do |ansible|
        ansible.playbook = "tests/test.yml"
       ansible.groups = { "test" => [ 'ubuntu' ] }
       ansible.verbose = 'vv'
       ansible.sudo = true
    end
end

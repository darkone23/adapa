# -*- mode: ruby -*-
# vi: set ft=ruby :

# Vagrantfile API/syntax version. Don't touch unless you know what you're doing!
VAGRANTFILE_API_VERSION = "2"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|

  config.vm.define :adapa do |node|
    node.vm.box = "precise-amd64"
    node.vm.box_url = "http://files.vagrantup.com/precise64.box"

    node.vm.hostname = "adapa"

    node.vm.provision :ansible do |ansible|
      ansible.playbook = "ansible/deps.yaml"
    end

    node.vm.provision :ansible do |ansible|
      ansible.playbook = "ansible/adapa.yaml"
    end
  end

  config.vm.define :oannes do |node|
    node.vm.box = "precise-amd64"
    node.vm.box_url = "http://files.vagrantup.com/precise64.box"

    node.vm.hostname = "oannes"

    node.vm.provision :ansible do |ansible|
      ansible.playbook = "ansible/deps.yaml"
    end

    node.vm.provision :ansible do |ansible|
      ansible.playbook = "ansible/adapa.yaml"
    end
  end

end

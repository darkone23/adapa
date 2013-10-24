# -*- mode: ruby -*-
# vi: set ft=ruby :

# Vagrantfile API/syntax version. Don't touch unless you know what you're doing!
VAGRANTFILE_API_VERSION = "2"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|

  config.vm.define :one do |config|
    config.vm.box = "precise-amd64"
    config.vm.box_url = "http://files.vagrantup.com/precise64.box"
    config.vm.hostname = "adapa-one"

    config.vm.provision :ansible do |ansible|
      ansible.playbook = "ansible/deps.yaml"
    end

    config.vm.provision :ansible do |ansible|
      ansible.playbook = "ansible/adapa.yaml"
    end
  end

  config.vm.define :two do |config|
    config.vm.box = "precise-amd64"
    config.vm.box_url = "http://files.vagrantup.com/precise64.box"
    config.vm.hostname = "adapa-two"

    config.vm.provision :ansible do |ansible|
      ansible.playbook = "ansible/deps.yaml"
    end

    config.vm.provision :ansible do |ansible|
      ansible.playbook = "ansible/adapa.yaml"
    end
  end

end

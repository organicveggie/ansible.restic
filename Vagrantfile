# -*- mode: ruby -*-
# vi: set ft=ruby :
Vagrant.configure("2") do |config|
  config.vm.define "ansible-restic"
  config.vm.box = "generic/ubuntu2004"

  config.vm.provision "ansible" do |ansible|
    ansible.playbook = "test.yml"
    ansible.config_file = "ansible.cfg"
    ansible.become = true
    ansible.extra_vars = "test-vars.yml"
    ansible.vault_password_file = "vault-passwd"
  end
end

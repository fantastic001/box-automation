# -*- mode: ruby -*-
# vi: set ft=ruby :

# Vagrantfile API/syntax version. Don't touch unless you know what you're doing!
VAGRANTFILE_API_VERSION = "2"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|
  config.vm.box = "jessie"
  config.vm.box_url = "https://ftp.lugons.org/vagrant/debian-8.0-x86_64.box"
  # config.vm.box_url = "https://dl.dropboxusercontent.com/s/60pv9an852jx9y0/Debian-7.3.0-i386b.box?dl=1" # for 32bit 
  config.vm.network :private_network, ip: "192.168.33.11"
  config.vm.provision :ansible do |ansible|
    ansible.playbook = "provision/site.yml"
    ansible.host_key_checking = false
  end
end

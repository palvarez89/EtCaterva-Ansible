# -*- mode: ruby -*-
# vi: set ft=ruby :

# Vagrantfile API/syntax version. Don't touch unless you know what you're doing!
VAGRANTFILE_API_VERSION = "2"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|

  config.vm.box = "ubuntu/trusty32"

  config.vm.define 'echaloasuerte1' do |machine|
    machine.vm.hostname = 'echaloasuerte1'
    machine.vm.network "private_network", ip: "192.168.77.22"


    machine.vm.provision :shell do |sh|
      sh.path = "bootstrap.sh"
      sh.args = "./ansible site.yml hosts_local"
    end
  end

end

Vagrant.configure("2") do |config|
  config.vm.box = "thoughtbot/ubuntu-14-04-server"
  config.vm.synced_folder ".", "/vagrant"

  config.vm.define "devbox01" do |devbox|
    devbox.vm.hostname = "dev.localhost.nl"
    devbox.vm.network :private_network, ip: "192.168.2.201"
    devbox.vm.provision "ansible" do |ansible|
      ansible.playbook = "playbook.yml"
      ansible.inventory_path = "hosts"
      ansible.limit = "192.168.2.201"
    end
  end

end
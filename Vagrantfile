box      = 'ubuntu/trusty64'
url      = 'https://atlas.hashicorp.com/ubuntu/boxes/trusty64'
hostname = 'ircbox'
domain   = 'example.com'
ip       = '172.0.0.100'
ram      = '1024'

Vagrant::Config.run do |config|
  config.vm.box = box
  config.vm.box_url = url
  config.vm.host_name = hostname + '.' + domain
  config.vm.network :hostonly, ip

  config.vm.provision "ansible" do |ansible|
      ansible.playbook = "playbook.yml"
  end
end

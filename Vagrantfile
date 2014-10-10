# -*- mode: ruby -*-
# vi: set ft=ruby :

VAGRANTFILE_API_VERSION = "2"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|
  config.vm.box = "hashicorp/precise32"

  config.vm.network "forwarded_port", guest: 3000, host: 8080

  config.vm.provision :chef_solo do |chef|
    chef.cookbooks_path = File.expand_path "../vendor/kitchen/cookbooks", __FILE__

    chef.json = {
      rbenv: {
        user_installs: [
          {
            user: 'vagrant',
            rubies: ['2.1.2'],
            global: '2.1.2',
            gems: { '2.1.2' => [
              { name: 'bundler' }
            ]}
          }
        ]
      }
    }

    chef.run_list = [
      'recipe[apt]', 
      'recipe[build-essential]', 
      'recipe[ruby_build]', 
      'recipe[rbenv::user]'
    ]
  end
end

VAGRANTFILE_API_VERSION = '2'

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|
  config.vm.box      = 'puppetlabs/centos-7.0-64-puppet'
  config.vm.hostname = 'jenkins'
  config.vm.network :private_network, ip: '33.33.33.10'

  config.vm.provider 'virtualbox' do |vb|
    vb.customize ['modifyvm', :id, '--memory', '1024']
  end

  config.vm.provision :puppet, :options => ['--debug', '--verbose', '--summarize', '--reports', 'store'] do |puppet|
    puppet.manifests_path = 'manifests'
    puppet.module_path    = 'modules'
    puppet.manifest_file  = 'base.pp'
  end

end

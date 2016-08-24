Vagrant.configure(2) do |config|

  config.vm.box = "dummy"
  config.vm.box_url = "https://github.com/mitchellh/vagrant-aws/raw/master/dummy.box"  

  config.vm.provider :aws do |aws, override|
   aws.access_key_id = ENV['AWS_KEY']
   aws.secret_access_key = ENV['AWS_SECRET']
   aws.keypair_name = ENV['KEY_NAME']
   aws.ami = "ami-fce3c696"
   aws.region = "us-east-1a"
   aws.security_groups = [ 'default' ]
   aws.instance_type = "m4.large"
#   aws.elastic_ip = "xx.xx.xx.xx"
   override.vm.box = "dummy"
   override.ssh.username = "ubuntu"
   override.ssh.private_key_path = ENV['KEY_PATH']
  end

  config.vm.provision "ansible" do |ansible|
    ansible.verbose = "v"
    ansible.playbook = "ansible/playbook.yml"
  end

end

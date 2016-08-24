# Vagrant-Ansible-AWS

### Prerequisite:
  1. Oracle Virtualbox
  2. Python
  3. Vagrant
  4. Ansible

  
### Ansible provisioning over AWS EC2 instance:
    Ansible provisioning is used to configure and setup AWS EC2 instance using vagrant-aws plugin.

```bash
$ export AWS_KEY="AWS api key" AWS_SECRET="AWS secret key" KEY_NAME="AWS key pair name" KEY_PATH="AWS .pem key path"
$ vagrant plugin install vagrant-aws
$ vagrant box add dummy https://github.com/mitchellh/vagrant-aws/raw/master/dummy.box
$ vagrant up --provider=aws
```

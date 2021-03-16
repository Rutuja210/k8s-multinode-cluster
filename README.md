# k8s-multinode-cluster

## goal: 
To create the k8s-multinode cluster with one master node and multiple worker/slave nodes

## pre-requisite:
- Install ansible and configure the configuration file for it which is in /etc/ansible directory
   [Refer this](./ip.txt)
- If you have to launch the ec2-instance on AWS by ansible then the IAM user with Administrator Access should be created.
- We need private key file with .pem extension to launch the ec2-instance. Take this file in your VM .
- We should have boto or boto3 package installed to do something in AWS. Use this command
  **_pip3 install boto_**  OR
  **_pip3 install boto3_**

## Solution:
- [Download this](./roles) directory in /etc/ansible/roles directory
- Configure the configuration file which is in /etc/ansible directory
   [Refer this](./ip.txt)
- Create the yaml file for launching the ec2-instances on AWS. 
  [node.yml file](./node.yml)
  Don't forget to add your access key and secret key of IAM user [in this file](./roles/kube_nodes/vars/main.yml)
- **_pip3 install boto_**  OR
  **_pip3 install boto3_**
  Install one of them which support to your OS.
- Now download [this yaml file](./node.yml) in you working directory and run it using the command 
  **_ansible-playbook node.yml_**
  And then the ec2-instance will launch on AWS
- Check your public IPs and update it in [this file](./ip.txt). Don't forget to update your private key file name also. [This file](./ip.txt) should be in the **/root** directory as we give this path in the [ansible conf file](./ansible.cfg)
- Now download [main yml file](./main_setup.yml) in working directory and run it by the command **_ansible-playbook main_setup.yml_**
- Now kubernetes multinode cluster is setup

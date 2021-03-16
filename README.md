# k8s-multinode-cluster

## goal: 
To create the k8s-multinode cluster with one master node and multiple worker/slave nodes

## pre-requisite:
- Install ansible and configure the configuration file for it which is in /etc/ansible directory
   [Refer this](./ip.txt)
- If you have to launch the ec2-instance on AWS by ansible then the IAM user with Administrator Access should be created.
- We need private key file with .pem extension to launch the ec2-instance. Take this file in your VM .
- We should have boto or boto3 package installed to do something in AWS. Use this command
  *_yum install boto_*  OR
  **yum install boto3**

## Solution:
- [Download this](./roles) directory in /etc/ansible/roles directory
- Configure the configuration file which is in /etc/ansible directory
   [Refer this](./ip.txt)
- Create the yaml file for launching the ec2-instances on AWS. 
  [node.yml file](./node.yml)
  Don't forget to add your access key and secret key of IAM user [in this file](./roles/kube_nodes/vars/main.yml)

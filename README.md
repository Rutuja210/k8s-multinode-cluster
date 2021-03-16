# k8s-multinode-cluster

## goal: 
To create the k8s-multinode cluster with one master node and multiple worker/slave nodes

## pre-requisite:
- Install ansible and configure the configuration file for it which is in /etc/ansible directory
   [Refer this](./ip.txt)
- If you have to launch the ec2-instance on AWS by ansible then the IAM user with Administrator Access should be created.
- We need private key file with .pem extension to launch the ec2-instance. Take this file in your VM .
- We should have boto or boto3 package installed to do something in AWS. Use this command
  **yum install boto**  OR
  **yum install boto3**

## Solution:
- [Download] (./roles) directory in /etc/ansible/roles directory

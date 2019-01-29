# aws-devops-demo
Demo of my knowledge on how to use Ansible to perform basic AWS tasks

AWS access key and secret key are stored in an encrypted file in location "group_vars/all/aws_cred.yml".
Replace with your own encrypted keys if you wish to test out the playbooks in this repo.

#############
TASKS DEMOD:
#############

Task: Provision an EC2 Instance
Command: ansible-playbook provision-ec2.yml --ask-vault --tags "<OS>"
Example:
  #Provision a new redhat EC2 instance
  ansible-playbook provision-ec2.yml --ask-vault --tags "redhat"
Notes: Available options for OS are 
  - amazon-linux-2
  - amazon-linux
  - suse
  - redhat
  - ubuntu-1804
  
#######

Task:

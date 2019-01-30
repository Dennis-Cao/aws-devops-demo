# aws-devops-demo
Demo of my knowledge on how to use Ansible to perform basic AWS tasks

AWS access key and secret key are stored in an encrypted file in location "group_vars/all/aws_cred.yml".
Replace with your own encrypted keys if you wish to test out the playbooks in this repo.

# Role List
- boot-ec2: Starts an existing EC2 instance
- create-ec2: Provisions a new EC2 instance
  - Can start five different OS types. Specified using tags. Available OS's are:
    - amazon-linux-2
    - amazon-linux
    - suse
    - redhat
    - ubuntu-1804
- shutdown-ec2: Shutsdown an existing EC2 instance
- download-s3: Downloads a pdf file from an S3 Bucket
- store-lambda-function-s3: (Unneccessarily) copies lambda function to EC2 instance, which then gets uploaded to S3
- 


# TASKS DEMOS


### Task: Provision an EC2 Instance
Command: ansible-playbook provision-ec2.yml --ask-vault --tags "\<OS>"\
Example:
  >#Provision a new redhat EC2 instance\
  ansible-playbook provision-ec2.yml --ask-vault --tags "redhat"
  


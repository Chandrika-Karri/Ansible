Ansible is used to automate tasks such as provisioning, configuration management, application deployment, orchestration, and continuous delivery. Using ansible playbook i had provisioned AWS resources like VPC, subnets, routetables, internet gateway, security groups, ec2 and s3. Used vault to store sensitive information like AWS access key and secret key. Vault is used to keep all your sensitive data in encrypted files. First create a vault file and set password for it. Follow the below steps:

ansible-vault create secrets.yml (prompts for password, set the password)
ansible-vault view secrets.yml
ansible-vault edit secrets.yml

Run the following command to execute the playbook
ansible-playbook -i hosts playbookname.yml --ask-vault-pass


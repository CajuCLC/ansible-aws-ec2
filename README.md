# ansible-aws-ec2

[![N|Solid](https://magebr.com/sites/default/files/Logo.png)](https://magebr.com/)

### Requirements
* Ansible 2.5+
* Boto 3 https://boto3.amazonaws.com/v1/documentation/api/latest/index.html
* AWS Credentials
* Git (terminal)

### Description
This Ansible playbook will create a security group, then an EC2 server and assign to the security group. This first commit only contains webserver, but we will add databases in the future (server or RDS).

### Installation
First install Boto 3:
```
pip install --upgrade pip
pip install boto3
```

Create the boto file:
```
vim ~/.boto
```

Use the following format:
```
[Credentials] 
aws_access_key_id = ACCESS_KEY 
aws_secret_access_key = SECRET_KEY
```

Set up your AWS credentials: https://docs.aws.amazon.com/cli/latest/userguide/cli-chap-getting-started.html

Clone this repository to your local environment:
```
git clone git@github.com:CajuCLC/ansible-aws-ec2.git
```

Edit the variables inside `ec2_vars/all.yml`
Run the playbook:
```
ansible-playbook -vvv -i hosts.yml aws-create.yml
```
That should be it. Have fun!

I'm following a short little course on Udemy
named Ansible for the Absolute Beginner - DevOps


I'll set up a Linux ec2 instance on my aws account
(I guess I could terraform it... 😄)

and look up how to install ansible and see how I do.

Wish me luck!

I started up an ec2 instance (Amazon Linux 2023 AMI 2023.4.20240319.1 x86_64 HVM kernel-6.1) and found this article:
https://medium.com/@dassandeep0001/install-ansible-on-ec2-instance-bbfa7e4481ec

This may help too:

https://docs.ansible.com/ansible/latest/installation_guide/intro_installation.html
https://docs.ansible.com/ansible/latest/installation_guide/installation_distros.html



```
sudo yum update -y

sudo yum install -y epel-release
sudo yum install -y ansible

ansible — version

sudo nano /etc/ansible/hosts

[your-group]
your-ec2-instance-ip-address
```
I'll have to keep in mind that this IP address will change each time.


## Run a very simple Ansible command

```
ansible localhost -m shell -a 'date'
ansible localhost -m shell -a 'pwd'
```

These give me info back:  Date
and
my working directory.



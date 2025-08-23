modules:
============
mongodb:
--------
copy
service
replace
dnf

catalogue:
---------
command
dnf
user
file
unarchieve
npm
systemd_service
service
command

redis:
-----
command
dnf
replace
lineinfile

cart:
------
command
dnf
user
file
unarchieve
npm
copy
systemd_service
service

mysql:
-----
command
dnf
service

frontend:
--------


user:
------
command
dnf
user
file
unarchieve
npm
copy
systemd_service
service
cart:
------
command
dnf
user
file
unarchieve
npm
copy
systemd_service
service

Dynamic inventory:
==================

inventory ----> static,hosts are fixed,

Auto scaling: ----> when tarffic increse infra also increse when traffic descrese infra alos decrease
ansible queries the ec2 instances based on some critiria.

now ansible needs to connect with ec2:
--------------------------------------
we need to install boto3 and botocore

filter:
us-east-1
running instances
name ---> frontend

file name should be ---> *.aws_ec2.yaml/yml 
plugin: adding extra functionlity to our code . it came from installltions(boto)

how ansible parallely connects to the ec2 instance:
--------------------------------------------------
using forks ---> how many number of instances ansible can connect
ANSIBLE_CONFIG ---> 1st preference
ansible.cfg ----> in the current directory
~/.ansible.cfg ---> in the home directory
/etc/ansible/ansible.cfg ----> last prefernce
ANSIBLE_CONFIG=/home/ec2-user/config/ansible.cfg
export ANSIBLE_CONFIG=/home/ec2-user/config/ansible.cfg
ansible --version

ansible-serial
------------
ex: we will take serial is 4 
so playbook run the play for every 4 instances

ansible can query the cloud provider to fetch hosts at run time this will useful in the autoscaling kind of dyanamic envi

aws can create aws infra
---------------------
for ansible everything is module if module is available it can create anything. Ansible may require libraries . to connect we need boto3 and botocore. aws configuration too

we will create
1. aws instances
2. route 53


keybased instaances:
------------------
we need to create a key and login ec2



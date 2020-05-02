Project Title
========================
Ansible is used for Software configuration purpose


installation 
===============================
$yum update -y && yum upgrade -y 

$yum install git -y && yum install wget -y && yum install unzip -y && yum install curl -y

$ yum install epel-release

add repo

vi /etc/yum.repos.d/ansible.repo

[Ansible]

name = ansible

baseurl = https://releases.ansible.com/ansible/rpm/release/epel-7-x86_64/

enabled = 1

gpgcheck = 0

$yum install ansible -y

Set up
=============================

Step 1: switch to root user

sudo su -l

passwd root

step 2: enable password authentication

vi /etc/ssh/sshd_config

PasswordAuthentication yes

permitroorlogin yes

systemctl restart sshd

step 3: generate ssh keys for key based authentication

ssh-keygen

ssh-copy-id root@localhost

Execution Flow
======================

step 1: clone repo

$git clone https://github.com/krishnamaram2/Configuration_Manager.git

Step 2:

$cd Configuration_Manager/src

$ansible-playbook -i hosts *.yml



Project Title
========================
Ansible is used for Software configuration purpose


 Pre-Requisites
===============================
$ sh hardening.sh
reference: https://github.com/krishnamaram2/WebApp

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



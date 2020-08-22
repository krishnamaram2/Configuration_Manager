Project Title
========================
Ansible is used for Software configuration purpose


 Pre-Requisites
===============================

step 1: enable password authentication

$vi /etc/ssh/sshd_config

   PasswordAuthentication yes

   permitroorlogin yes

$systemctl restart sshd

step 2: generate ssh keys for key based authentication

ssh-keygen

Step 3: add ssh keys 

ssh-copy-id centos@localhost

Step 0: add public keys

 #!/bin/bash
 
 ssh-keygen -q -t rsa -N '' -f /home/centos/.ssh/id_rsa <<<y 2>&1 >/dev/null

 cat /home/centos/.ssh/id_rsa.pub >> /home/centos/.ssh/authorized_keys

 ssh -o StrictHostKeyChecking=no centos@localhost


Execution Flow
======================

step 1: clone repo

$git clone https://github.com/krishnamaram2/configuration-manager.git

Step 2: run playbooks

$cd configuration-manager/src/webapp

$ansible-playbook -i hosts plays/webapp.yml




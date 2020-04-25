Project Title
========================
Ansible is used for Software configuration purpose


installation and set up
===============================
$yum update -y && yum upgrade -y 
$yum install git -y && yum install wget -y && yum install unzip -y && yum install curl -y
$yum install ansible -y

step 1:
$sudo yum install ansible -y

step 2:
vi /etc/ssh/sshd_config
PasswordAuthentication yes
permitroorlogin yes

systemctl restart sshd

step 3:
ssh-keygen
ssh-copy-id user@hostip


step 4:
ansible-playbook -i hosts sample.yml







remote_user
become_user
become: yes
become_mathod:sudo











site.yml

roles/

     common
     
     webserver
     
     appserver
     
     dbserver
   

https://github.com/ansible/ansible-examples/blob/master/language_features/postgresql.yml
http://www.wiivil.com/installing-mysql-on-centos-7-server-using-ansible/


---
-  hosts : dbserver
   become: yes
   vars:
     mysql_root_password: root
   tasks:
    - name: create database
      mysql_db: name=indigo state=present

    - name: create mysql user
      mysql_user:
           name: krishna
           password: Krishna_123
           priv: '*.*:ALL'
           state: present
           login_user: root
           login_password: "{{mysql_root_password}}"
    - name: install git
      yum: name=git state=present
    - name: clone WebApp repo
      git: repo=https://github.com/krishnamaram2/WebApp.git dest=/root/WebApp
    - name: import indigo.sql
      shell: mysql -u krishna -pKrishna_123 indigo < /root/WebApp/binary/indigo.sql








#Project Title
Ansible is used for Software configuration purpose


installatiion ansible
====================

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
   

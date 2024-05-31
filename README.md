# RHEL
RHEL/Fedora RPM for Ansible

This repo has instructions for the creation of signature RPM's useful with RHEL v8/v9 and Fedora.
It's a SystemD complient Service/Deamon which logs it's activities into the syslog
Deployable via Ansible.

#Tested with RHEL v9#

#Build instructions:
sudo dnf install rpm-build rpmdevtools
sudo dnf install rpm-build rpmdevtools

gcc -o hello hello.c

tar -czvf hello-1.0.tar.gz hello.c hello hello.service 

rpmbuild -bb hello.spec
rpmbuild -bb ../SPECS/hello.spec

#Install / remove
sudo rpm -ivh hello-1.0-1.el9.x86_64.rpm
sudo rpm -e hello

#Check installed and version
rpm -q hello

#Ansible:

Hosts definition:
[meine_server]
zielhost1 ansible_host=220.240.130.248 ansible_user=dravion

#Then execute for Network deployment
ansible-playbook -i hosts playbook.yml --ask-become-pass



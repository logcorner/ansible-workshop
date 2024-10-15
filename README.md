# ansible-workshop

https://docs.ansible.com/ansible/latest/playbook_guide/playbooks_intro.html#playbook-syntax

https://github.com/g0t4/course-ansible-getting-started

git config --global user.name "logcorner"
git config --global user.email "tocane.technologies@gmail.com"
git config --global --list

ansible-playbook playbook.yml 
ansible-playbook playbook.yml  -vvv

ansible-doc copy


ansible-inventory --list



cd sources/repos/ansible-workshop/'Getting Started with Ansible'

ssh-copy-id -i ~/.ssh/id_rsa.pub logcorner@20.82.123.107


ssh -i ~/.ssh/id_rsa.pem logcorner@20.82.123.107

ansible -i ~/my_inventory.ini -m ping ubuntu_nodes


ansible-playbook -i custom_inventory.ini playbook.yml

# INVENTORY


ansible-inventory --list

# Playbooks
Ansible Playbooks

Exchange Keys: ssh-keygen -t rsa -b 2048
ssh-copy-id node1

copy /etc/hosts/* to Ansible directory
change ansible.cfg
    inventory = hosts (tells it to look in the root directory of the ansible directory)

modify hosts file to list inventory in INI format (Ansible/hosts)

run shell command ad-hoc
    ansible all -m shell -a "uptime"

Failed to connect to the host via ssh: Permission denies (publickey,password)
    nano hosts
        [local]
        localhost ansible_connection=local


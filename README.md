# Playbooks
modify /etc/hosts on the controller to have private IP addresses of all nodes

Ansible Playbooks

Exchange Keys: ssh-keygen -t rsa -b 2048
ssh-copy-id node1..3

copy /etc/hosts/* to Ansible directory
change ansible.cfg
    inventory = hosts (tells it to look in the root directory of the ansible directory for the hosts file)

modify hosts file to list inventory in INI format (Playbooks/hosts)

run shell command ad-hoc
    ansible all -m shell -a "uptime"

Failed to connect to the host via ssh: Permission denies (publickey,password)
    nano hosts
        [local]
        localhost ansible_connection=local

https://github.com/openstack/ansible-hardening

Installing Ansible Hardening roles from Openstack using ansible-galaxy
    ansible-galaxy install git+https://githubl.com/openstack/ansible-hardening

or using git
    mkdir -p ~/.ansible/roles/
    git clone https://github.com/openstack/ansible-hardening ~/.ansible/roles/ansible-hardening

#############################################################################################################

Configure Dnsmasq as a DNS server on Host 1

Add group dns servers to hosts file

run dns.yml playbook

##############################################################################################################

add ansible galaxy module

ansible-galaxy collection install community.general


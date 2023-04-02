# ansible

NVENTORY : Inventory is nothing but the list of machine ip or dns names that you want ansible to be managed
Ansible by default installs 2.9 as by default on AMI's we will get python2. Always go with latest version, which can be installed from tools/ansible/install.sh

all is a group which included all the entries in INVENTORY File

ANSIBLE has lot of pre-defined variables and we need to use them to supply userName and password it has to use to authenticate to the nodes.

ansible_user : Predefined variable for userName
ansible_password : Predefined variable for password

Variables should be passed to ansible by using the flag -e 
    
    Ex: ansible -i INVENTORY all  -e ansible_user=userName -e ansible_password=password 
    $ ansible -i inv all  -e ansible_user=centos -e ansible_password=xyz123 -m shell -a uptime

Ansible is a collection of modules / collections : Whatever the task that you want to perform is already predefined, all you need is just to consume them.

There 1000's of modules available : -m shell. -m yum , -m service

Ansible can be executed in 2 ways :
1) Manual Approach      : using ansible command  : With this you can execute one command at time.
2) Automated Approach   : using ansible playbook : With this we can mention all the set of tasks that needs to be executed, things will happen in the declared approach 

Playbooks are written using a language called YAML.

YAML is just  markup languaga ; Markup language is nothing a presentation language


# ansible-getting-started
Getting started and running ansible on managed nodes. 

To configure this playbook:

1. Create a `hosts` file from etc_example/hosts, change the info according to your environment.
2. Make sure the `ansible_ssh_user` you defined in  `hosts` have sudo privilege on target nodes.

## netplan for ubuntu
```
cd playbooks/netplan/
ansible-playbook -i inventory main.yml -kK
```

## setup ssh
```
ansible-playbook -i etc_example/hosts playbooks/setup_ssh.yml -kK
```

## bootstrap servers
```
ansible-playbook -i etc_example/hosts site.yml
```

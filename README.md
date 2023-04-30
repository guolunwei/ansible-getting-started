# ansible-getting-started
To get up and running ansible on managed nodes.

## test connection
```
ansible -i hosts all -m ping -k
```

## setup environment
```
ansible-playbook -i hosts site.yml -kK
```

> Note: To run this playbook, you need to have a user with sudo privilege on managed nodes at first. And the user needs be defined by `ansible_ssh_user` in the `hosts` file. 


How To Configure Apache Using Ansible on 
    https://www.digitalocean.com/community/tutorials/how-to-configure-apache-using-ansible-on-ubuntu-14-04

LEMP
    https://www.digitalocean.com/community/tutorials/how-to-install-linux-nginx-mysql-php-lemp-stack-ubuntu-18-04

# ansible command
ansible -m ping all

ansible [name] -m ping

ansible -m shell -a 'hostname' all

ansible -m shell -a 'df -h' all

ansible-playbook [name].yml

# linux command

切換成 root 權限

```sudo -s```

磁碟列表(含未mount)

```fdisk -l```

掛載磁碟列表

```df -h```

系統排程

修改

```crontab -e```

查看

```crontab -l```

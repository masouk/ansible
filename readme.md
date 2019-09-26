
How To Configure Apache Using Ansible on 
    https://www.digitalocean.com/community/tutorials/how-to-configure-apache-using-ansible-on-ubuntu-14-04

LEMP
    https://www.digitalocean.com/community/tutorials/how-to-install-linux-nginx-mysql-php-lemp-stack-ubuntu-18-04

## ansible command


#### 檢查所有連線

	ansible -m ping all
	
#### 確認主機是否可以連線

	ansible {name} -m ping
	
#### 跑遠端 shell

	ansible -m shell -a 'hostname' all
	ansible -m shell -a 'df -h' all
	
#### 執行遠端部屬

	ansible-playbook [name].yml

## linux command

#### 切換成 root 權限

	sudo -s

#### 磁碟列表(含未mount)

	fdisk -l

#### 掛載磁碟列表

	df -h

#### 系統排程

	// 修改
	crontab -e
	
	// 查看
	crontab -l

#### 查看 PORT 的 pid
	lsof -i:{PORT}

#### 刪除 pid
	kill -9 {pid}



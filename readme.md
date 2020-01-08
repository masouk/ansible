
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
	
	// -i 連線檔案位置
	ansible-playbook [name].yml -i hosts --user [username] --ask-pass --ask-become-pass

## docker command

#### rum image and background run

	docker run -td --name [container_name] -v [local_path]:[remote_path] [image_id]
	
	docker exec -it [container_id] bash

## linux command

#### 切換成 root 權限

	sudo -s

#### 磁碟列表(含未mount)

	fdisk -l

#### 磁碟掛載

<https://cloud.google.com/compute/docs/disks/add-persistent-disk?hl=zh-tw>

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
	
#### 記憶體狀況
	free -m
	
#### 預設套件版本查看
	apt show php
	apt-cache policy nodejs
	
#### 作業系統
	uname -a
	cat /etc/lsb-release
	
#### 清除 log 下 .gz 之檔案
	sudo find /var/log/ -type f -regex '.*\.[0-9]+\.gz$' -delete
	
## GIT
	// first commit reset 
	git update-ref -d HEAD
	
	// 多 commit 整併
	git rebase -i {log-id}

## Jupyter remote connection
	// remote
	jupyter notebook --no-browser --port=8889
	
	// local 
	// options: -N: 建立通道，但不連進SSH服務器裡; -f: 背景執行(不顯示LOG)，terminal 關掉即結束; -L: 正向連線 -R: 反向連線
	ssh -N -f -L localhost:8888:localhost:8889 username@your_remote_host_name
	


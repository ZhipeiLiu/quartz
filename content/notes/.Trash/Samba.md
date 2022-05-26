Samba + 开机自mount + 一键安装nextcloud


## 安装samba
安装
`sudo apt-get install samba`
相关支持工具
`sudo apt-get install samba-common-bin`
编辑config
`sudo nano /etc/samba/smb.conf`
```
[share]           #共享文件的名称， 将在网络上以此名称显示
path = /home/pi/Desktop/         #共享文件的路径，我们默认使用桌面文件夹
valid users = pi        #允许访问的用户
browseable = yes        #允许浏览
public = yes        #共享开放
writable = yes        #可写
```
增加samba用户
`sudo smbpasswd -a pi`
重启
`sudo systemctl restart smbd.service`

## 开机自动mount + Samba
[CSDN](https://blog.csdn.net/mochou111/article/details/81298613)
mkdir /mnt/u01 
sudo chmod 777 /mnt
sudo chmod 777 /mnt/u01


sudo chmod -R 777 

记得用sudo
```
fdisk -l                       # 查看可挂载的磁盘
df -h                          # 查看已经挂载的磁盘
mkfs.ext4 /dev/vdb  # 初始化磁盘,格式是ext4,注意这里会格式化可挂载磁盘(需要先unmount)
mount /dev/vdb /u01  # mount 磁盘到/u01，保证/u01为空
blkid                         # 获取磁盘的uuid和属性，用uuid来进行开机mount
sudo vim /etc/fstab          # 开机mount，模板是UUID=********** /u01 ext4 defaults 1 1 
```
3120eab6-0e86-4c2f-b0f0-7bd52535fab5
[浅析 fstab 与移动硬盘挂载方法](https://www.cnblogs.com/mq0036/p/11919338.html)
## 一键安装nextcloud
[博客](https://blog.ee-fans.com/index.php/树莓派所有版本一键安装nextcloud/)
#### 更新系统
`sudo apt-get update`
`sudo apt-get upgrade`
#### 安装Ansible
`sudo apt-get install ansible -y`
#### 下载脚本
`git clone https://github.com/ZhipeiLiu/raspi_nextcloud.git`
`cd raspi_nextcloud`
#### 安装
```
date ; ansible-playbook --become -c local -i "localhost," --extra-vars "DATABASE=mysql MYSQL_ROOT_PASSWORD=qwerty NCUSER_PASSWORD=raindrop" build_nextcloud.yml
```
- MySQL root用户密码：qwerty（可自行修改MYSQL_ROOT_PASSWORD=qwerty）
- nextcloud数据库用户：**ncuser**（可通过修改脚本源码修改）
- nextcloud数据库密码：**raindrop** (可自行修改NCUSER_PASSWORD=raindrop)
- nextcloud数据库名：**nextcloud**（可通过修改脚本源码修改）
#### 配置安装
`http://192.168.0.167/nextcloud`
Create Account:
liuaoo
Liuzhipei861bh
Data Folder: `/var/nextcloud/data`
ncuser
raindrop
nextcloud
localhost
#### 挂载外部磁盘-本地
进入应用-enable External Storage Support- 并从设置打开
外部存储添加：
目录名称：Matt
增加存储：本地
配置：/mnt/u01
分组：配置
test connectivity
#### 从外部连接
[CSDN](https://blog.csdn.net/William_Lee1333/article/details/104652649)
mttt.ddns.net:8000/nextcloud
sudo nano /var/www/html/nextcloud/config/config.php
添加：
```
	  'trusted_domains' =>                    
	  array (                                          0 => 'localhost',                                                           
	    1 => 'nextcloud.companyname.com',         
	    2 => preg_match('/cli/i',php_sapi_name())?'127.0.0.1':$_SERVER['SERVER_NAME'],                                                     
  ), 
```

`2 => preg_match('/cli/i',php_sapi_name())?'127.0.0.1':$_SERVER['SERVER_NAME'], `

[nextcloud提示您没有权限在此上传或创建文件](https://blog.csdn.net/STL_CC/article/details/105606816)

qq邮箱密码
arhvkfosjbksbdad
发送邮件服务器：smtp.qq.com，使用SSL，端口号465或587

sudo wget -N --no-check-certificate https://raw.githubusercontent.com/ToyoDAdoubi/doubi/master/aria2.sh && sudo chmod +x aria2.sh && sudo bash aria2.sh

[解决GitHub的raw.githubusercontent.com无法连接问题](https://www.cnblogs.com/sinferwu/p/12726833.html)


## Aria2 download
开机运行
aria2c --conf-path /etc/aria2.conf

## 运行occ脚本
sudo -u www-data php /var/www/html/nextcloud/occ maps:scan-photos

[一键安装脚本](https://github.com/P3TERX/aria2.sh)
安装依赖
`sudo apt install wget curl ca-certificates`
下载脚本
`sudo wget -N git.io/aria2.sh && chmod +x aria2.sh`
运行脚本
`sudo ./aria2.sh`

Aria2 简单配置信息：
```
 IPv6 地址	: 188.119.65.15
 RPC 端口	: 6800
 RPC 密钥	: 5a1f84b1bdf431a92c47
 下载目录	: /root/downloads
```

https://v.mattzo.com/M.dmg


维护模式
sudo -u www-data php /var/www/html/nextcloud/occ maintenance:mode --off

## [离线安装nextcloud应用]
https://www.jianshu.com/p/24f66d0d2660)

ocDownloader 配置Nextcloud离线下载功能
https://www.orgleaf.com/2743.html

安装aira2及开机启动配置
https://blog.csdn.net/passball/article/details/83317910
https://www.jianshu.com/p/3c1286c8a19d

SS:
https://www.whrblog.online/archives/573

/Volumes/My Passport/Music/

/Volumes/My Passport/Music/Processed NCM


{
  "server":"104.128.95.11",
  "local_address": "127.0.0.1",
  "local_port":1080,
  "server_port":6578,
  "password":"3O0YA8PRThCCkQa9",
  "timeout":300,
  "method":"aes-256-gcm"
}

{
  "server":"ru01.clashcloud.club",
  "local_address": "127.0.0.1",
  "local_port":1080,
  "server_port":28263,
  "password":"l0kbGN",
  "timeout":300,
  "method":"rc4-md5"
}

sslocal -s ru01.clashcloud.club -p 28263 -k l0kbGN -m rc4-md5

https://floperry.github.io/2019/02/24/2018-06-25-Ubuntu-18.04-下解决-shadowsocks-服务报错问题/


开启：
https://blog.chaos.run/dreams/debian-shadowsocks-libev-client/



## Linux安装Collabora Online让NextCloud支持Office在线编辑
https://jszbug.com/10563
## 安装shadowsocks
Linux 使用 Shadowsocks 设置教程:
https://shadowsockshelp.github.io/Shadowsocks/linux.html#命令行客户端
命令行安装
```
apt-get install python-pip
pip install git+https://github.com/shadowsocks/shadowsocks.git@master
```


https://ruanx.net/pi-hole/

sudo cp -rf /mnt/u01/AdminLTE-master/* /var/www/html/admin




MySQL application password for phpmyadmin:    
Liuzhipei861bh

mysql> UPDATE user SET Password=PASSWORD('raindrop') WHERE USER='root' and host='root' or host='localhost';




树莓派calibre
https://post.smzdm.com/p/aekep89z/


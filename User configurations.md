### User add in web server and configuration
```shell
sudo su
useradd ansadmin
passwd ansadmin
```
### need some changes for login with this user
```shell
cd  /etc/ssh/ssh_config
vi /etc/ssh/ssh_config
```
### uncomment line
```shell
71 PasswordAuthentication yes // uncomments this line
72 #PermitEmptyPasswords no
73 #PasswordAuthentication no // comments this line

```
### Restart sshd
```shell
service sshd restart
```

---------ansible server -----------

ssh-keygen





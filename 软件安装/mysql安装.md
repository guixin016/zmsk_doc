### mysql安装 ###
----

### 1、安装mysql

```
 # wget http://dev.mysql.com/get/mysql-community-release-el7-5.noarch.rpm
 # rpm -ivh mysql-community-release-el7-5.noarch.rpm
 # yum install mysql-community-server
```

### 2、安装成功后启动mysql

```
service mysqld restart
```

### 3、设置密码

```
mysql> UPDATE mysql.user SET Password = PASSWORD('newpwd') WHERE User = 'root';

mysql> FLUSH PRIVILEGES;
```

### 4、设置mysql编码

mysql配置文件为/etc/my.cnf,最后加上编码配置

```
[mysql]
default-character-set =utf8
```

### 5、创建远程连接

把在所有数据库的所有表的所有权限赋值给位于所有IP地址的root用户。

```
mysql> grant all privileges on *.* to root@'%'identified by 'password';
```

如果是新用户而不是root，则要先新建用户

```
mysql>create user 'username'@'%' identified by 'password';  
```

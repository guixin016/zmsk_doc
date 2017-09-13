### jetty部署文档###
-----
#### 1、下载安装jetty

1、下载jetty

```
wget http://central.maven.org/maven2/org/eclipse/jetty/jetty-distribution/9.4.2.v20170220/jetty-distribution-9.4.2.v20170220.tar.gz
```

2、解压jetty压缩包

```
# cd /usr/local   切换到 /usr/local 目录下
# tar -zxvf jetty-distribution-9.4.2.v20170220.tar.gz  解压压缩文件
```


#### 2、部署应用程序

1、创建存放应用程序的目录

应用程序一般放在/home/pft 目录下，目录不存在则创建

```
# cd /home/pft
```

创建文件目录，目录名称规范(项目名_base)

```
# mkdir pft_rest_base
# cd pft_rest_base
# mkdir logs   创建日志文件存储目录
# mkdir webapps
# cd webapps
# mkdir ROOT  创建应用程序编译打包后文件存放的目录
```

拷贝jetty的start.init文件到项目文件夹下,编辑start.init文件，修改项目使用的端口号

#### 3、jetty启动应用程序

切换到logs文件目录下启动程序
```
# cd /home/pft/pft_rest_base/logs 
# nohup java -jar /usr/local/jetty9/start.jar jetty.base=/home/pft/pft-rest-base &
```

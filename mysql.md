# win

---

```
一些报错整理：
1.查看mysql配置文件目录
select @@mysqldir

2.connector/odbc 安装失败
缺少常用运行库

3.客户端连接mysql报错1042
netsh winsock reset
```

# linux

---

```
切换用户
sudo su

安装软件
sudo apt install mysql-server mysql-client 

安装过程
中间会提示输入 root 密码

操作
mysql -uroot -p
show databases;

修改配置文件
/etc/mysql/mysql.conf.d/mysqld.cnf

修改可请求 ip 地址
bindadress

重启
sudo service mysql restart
```

# mac

---

```
安装
brew install mysql

操作
同 linux
```




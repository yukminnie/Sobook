# linux

---

```
安装
sudo apt install redis-server

启动
redis-cli

操作
set 'a' 'b'

get 'a'

结束
ctrl + c

配置
sudo vi /etc/redis/redis.conf 

设置远程连接
注释掉 bind 127.0.0.1

设置远程连接密码
requirepass foodared  --->  requirepass <mypassword>

重启 redis
sudo service redis restart

启动密码进入
redis-cli -a <mypassword>
```

# mac

---

```
安装
brew install redis

配置
usr/local/etc/redis.conf

配置 操作方法
同 linux

查看 redis 服务的状态
brew services list

重启 redis
brew services restart redis
```

# win

---

```
软件操作  不再敖述
```




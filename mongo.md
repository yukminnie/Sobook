# 只谈一下 Mongo。

# windows

---

#### Mongo 安装完成后建立数据存储目录，并在命令行进行设置

```
$ C:\MongoDB\Server\3.4\bin
$ mongod --dbpath C:\MongoDB\Server\3.4\data\db
```

#### 然后程序给我们开放了本地27017端口

```
$ 2017-06-16T20:06:28.613+0800 I NETWORK  [thread1] waiting for connections on port 27017
```

#### 重开一个命令行，输入命令可以进入数据库操作模式

```
$ C:\MongoDB\Server\3.4\bin
$ mongo
```

#### 但我们通常是将 Mongo 配置好，使用客户端进行操作。因此我们建立日志存储目录，并新建文件 mongo.log，然后管理员模式运行命令行

```
$ C:\MongoDB\Server\3.4\bin
$ mongod --bind_ip 0.0.0.0 --logpath C:\MongoDB\Server\3.4\data\logs\mongo.log --logappend --dbpath C:\Mon goDB\Server\3.4\data\db --port 27017 --serviceName 'MongoDB' --serviceDisplayName 'MongoDB' --install
```

PS：此处 mongo.log的文件路径必须通过「属性-安全-对象名称」复制获取，绑定 0.0.0.0 表示接受任意ip管理，「--logappend」表示以从属的模式跟随在「dbpath」后，最后给服务定义名称

#### 接着我们在「计算机管理-服务」中启动Mongo服务，并可设置其为开机启动，然后使用客户端 Robomongo 进行连接管理。

```
PPS: Mysql 默认端口 「locahost : 3306」      Redis 默认端口 「localhost : 6379 , 接受任意ip管理需编辑conf文件」
```

---

# linux

---

```
安装
sudo apt install mongodb

启动
mongodb

进入命令行
mongo

显示数据库
show dbs

使用
use local
```

---

# mac

---

安装homebrew ,参考unix\_book

```
安装
homebrew install mongodb

首先会自动安装 openssl 依赖

If you need to have this software first in your PATH run:
  echo 'export PATH="/usr/local/opt/openssl/bin:$PATH"' >> ~/.bash_profile
```




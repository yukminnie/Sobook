## linux

```
查询位置命令

find / -name '命令名称'

查询mysql位置命令

which mysql

服务管理命令

sudo apt install sysv-rc-conf

sudo sysv-rc-conf

空格可以在图形界面中进行反选

service '服务名' status

linux启动步骤

1. 读取 MBR 的信息,启动 Boot Manager
        Windows 使用 NTLDR 作为 Boot Manager,如果您的系统中安装多个
        版本的 Windows,您就需要在 NTLDR 中选择您要进入的系统。
        Linux 通常使用功能强大,配置灵活的 GRUB 作为 Boot Manager。
2. 加载系统内核,启动 init 进程
        init 进程是 Linux 的根进程,所有的系统进程都是它的子进程。
3. init 进程读取 /etc/inittab 文件中的信息,并进入预设的运行级别,
   按顺序运行该运行级别对应文件夹下的脚本。脚本通常以 start 参数启
   动,并指向一个系统中的程序。
        通常情况下, /etc/rcS.d/ 目录下的启动脚本首先被执行,然后是
        /etc/rcN.d/ 目录。例如您设定的运行级别为 3,那么它对应的启动
        目录为 /etc/rc3.d/ 。
4. 根据 /etc/rcS.d/ 文件夹中对应的脚本启动 Xwindow 服务器 xorg
        Xwindow 为 Linux 下的图形用户界面系统。
5. 启动登录管理器,等待用户登录
        Ubuntu 系统默认使用 GDM 作为登录管理器,您在登录管理器界面中
        输入用户名和密码后,便可以登录系统。(您可以在 /etc/rc3.d/
        文件夹中找到一个名为 S13gdm 的链接)


ps：在Debian Linux中，下列路径对应不同的运行级别。当系统启动时，通过其中的脚本文件来启动相应的服务。 
/etc/rc0.d Run level 0 
/etc/rc1.d Run level 1 
/etc/rc2.d Run level 2 
/etc/rc3.d Run level 3 
/etc/rc4.d Run level 4 
/etc/rc5.d Run level 5 
/etc/rc6.d Run level 6 

Ubuntu默认是在runlevel 2启动的，那么我们之需要修改rc2.d中的文件，从而禁止某些服务启动

6. unable to resolve host 报错

        127.0.0.1 localhost <主机名>

7. 添加用户

        sudo adduser <name>
       usermod -aG sudo ghost


8. 文件权限临时关闭,结束后重新打开

        chmod -R 777 <DIR>

        chmod -R 644 <DIR>
        
        sudo chown user:user /data/wwwroot/ghost

9. kpkg资源被锁安装无法进行

        sudo rm /var/cache/apt/archives/lock
        sudo rm /var/lib/dpkg/lock

9. 完整复制文件夹

        cp -R 源目录/* 目地目录

10. NPM gets killed no matter what，内存不足

        dd if=/dev/zero of=/var/swap bs=1k count=1024k
        mkswap /var/swap
        swapon /var/swap
        echo '/var/swap swap swap default 0 0' >> /etc/fstab

11. ubuntu更新报错 dpkg was interrupted

        cd /var/lib/dpkg/updates
        rm -rf *
        sudo apt-get upgrade
        sudo apt-get update
12. npm v6 安装

        curl -sL https://deb.nodesource.com/setup_6.x | bash -  
        apt-get install nodejs
        
13. npm淘宝源
        npm --registry https://registry.npm.taobao.org info underscore  
        

14. yarn
        curl -sS https://dl.yarnpkg.com/debian/pubkey.gpg | sudo apt-key add -
        echo "deb https://dl.yarnpkg.com/debian/ stable main" | sudo tee /etc/apt/sources.list.d/yarn.list
```




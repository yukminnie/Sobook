# SSH Key ，适用于 Coding.net

---

####Git安装完成后，打开命令行
```
$ ssh-keygen -t rsa -C "这里填写你的邮箱地址"
```

####伴随两次确定（尽量不要设置密码），SSH Key生成于 ./ssh 目录下，我们将 id _rsa 中的文本复制到 github 和 coding

```
$ git config --global user.name “your_username”  #设置用户名
$ git config --global user.email “your_registered_github_Email” 
#设置邮箱地址(建议 giuhub 和 coding 使用同样的邮箱，避免不必要的麻烦)
```

####最后，测试连接

```
$ ssh -T git@github.com
$ ssh -T git@git.coding.net

```
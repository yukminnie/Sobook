1.安装xadmin

2.setting中引入app:xadmin, crispy_forms

3.admin中删除之前注册的model

```
注意,此时虽然我们删除了UserProfile,但是xadmin仍然会发现它,并将它注册到后台
```

4.urls中插入xadmin,修改xadmin.site.url

5.xadmin安装成功后,会存在一些默认的表,我们对xadmin进行数据库同步

```
存在三张表:
bookmark, usersettings, userwidget

makemigrations
migrate
```

6.我们通过git下载xadmin,我们将解压后的xadmin文件夹,复制到项目根目录之下

7.我们建立extra_apps package目录,通过它管理第三方插件包,然后我们拖入admin,并mark source root

8.此时我们可以通过项目引用xadmin,我们卸载admin

9.我们打开后台,发现界面有所改变(不一定一直有改变,只是源码此时比较新,还没有通过pypi发布)


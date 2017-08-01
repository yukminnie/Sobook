1.安装xadmin

2.setting中引入app:xadmin, crispy_forms

3.admin中删除之前注册的model

```
注意,此时虽然我们删除了UserProfile,但是xadmin仍然会发现它,并将它插入后台
```

4.urls中插入xadmin,修改xadmin.site.url

5.xadmin安装成功后,会存在一些默认的表,我们对xadmin进行数据库同步

```
存在三张表:
bookmark, usersettings, userwidget

makemigrations
migrate
```


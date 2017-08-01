1.安装xadmin

2.setting中引入app:xadmin, crispy_forms

3.admin中删除之前注册的model

4.urls中插入xadmin,修改xadmin.site.url

5.对xadmin进行数据库同步

```
makemigrations
migrate
```


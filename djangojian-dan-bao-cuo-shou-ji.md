#报错收集
---

### url无法匹配

```
输入错误网址
```

### 模版丢失

```
'DIRS': [os.path.join(BASE_DIR, 'templates')]
```
### 没有样式

```
STATICFILES_DIRS = [
    os.path.join(BASE_DIR, 'static')
]
```
### 数据库同步无效

```
注册app 到settings
```


### 连接到数据到数据库出错

先安装mysql-python

```
DATABASES = {
    'default': {
        'ENGINE': 'django.db.backends.mysql',
        'NAME': "testdjango",
        'USER': "root",
        'PASSWORD': "000006",
        'HOST': "127.0.0.1"
    }
}

```

### 引入麻烦

```
Mark Directory as source root
```

### 简单流程梳理

![](/assets/2017-07-30_164152.png)


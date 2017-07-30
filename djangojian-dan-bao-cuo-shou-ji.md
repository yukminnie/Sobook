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

### 插入数据到数据库出错

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
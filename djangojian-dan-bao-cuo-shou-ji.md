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
### 数据库同步出错

python2 指定中文编码
```
# _*_ coding:utf-8 _*_
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

### 常见的model类型

```
CharField
IntergerField

SmallIntegerField
BigIntegerField

DateTimeField
ImageField
TextField
FileField

BooleanField

FieldDoesNotExist


FilePathField
URLField
IPAdreessField
EmeialField
ForeignKey
```

### 关于主键
数据库会自动添加id主键，我们也可以自定义主键,要有长度，要有默认值

```
object_id = models.CharField(max_length=50, default='', primary_key=Ture, verbose_name=u'主键')
```

### 关于Meta
我们可以指定其数据库名，和字段排列方式

```
db_table = 'user_message'
orderding = '-object_id'
```

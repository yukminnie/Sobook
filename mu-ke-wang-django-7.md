1.后台管理系统特点

```
权限管理

少前端样式

快速开发
```

2.setting文件自带app分析

```
django.contrib.admin        ------> admin.site.urls
django.contrib.auth
django.contrib.contenttypes    
django.contrib.sessions
django.contrib.messages
django.contrib.staticfiles

```

3.createsuperuser报错

```
#报错(查明应该是自定义长度和数据本身不符,来源于gender(famale 女)
data too long for column,修改完成要进行数据库同步

#修改后同步,可能报错,也可能不报错

报错原因:合并app之前进行的数据库同步



sql-mode=”STRICT_TRANS_TABLES,NO_AUTO_Create_USER,NO_ENGINE "中的stric_trans_tables去掉，关闭严格模式，重启数据库

#报错，不管了(应该是和第一个报错原因一致)
 Warning: Data truncated for column 'gender' at row 1
  return self.cursor.execute(query, args)
```

4.更改中文

```
LANGUAGE_CODE = 'zh-hans'    

TIME_ZONE = 'Asia/Shanghai'

USE_TZ = False      #关闭utc时区

```

5.注册model并为model定义管理器

```
from .models import UserProfile


class UserProfileAdmin(admin.ModelAdmin):
    pass

admin.site.register(UserProfile, UserProfileAdmin)

```

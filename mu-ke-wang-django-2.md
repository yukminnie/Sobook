1.PEP8 模块的导入顺序

```
系统 > 第三方 > 自建
```

2.导入时间模块

```
from datetime import datetime
```

3.定义EmailVerifyRecord

```
code 验证码 CharField
email 邮箱 EmailField
send_type 发送状态 CharField choices
seng_time 发送时间 default=datetime.now

#注意：此时datetime.now()会返回model修改时间
```


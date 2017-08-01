1.将建立的app加入到新的apps package文件夹中

```
search for references

open moved files in eitor
```

2.将apps目录mark as sources root

3.setting设置

```
import sys

sys.path.insert(0, os.path.join(BASE_DIR, 'apps'))
```

4.debeg
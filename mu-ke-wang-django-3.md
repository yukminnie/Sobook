1.user 同级目录建立course 目录
```
第一层：course.model
第二层：lesson.model video.model courseresource
```

2.Course.model

```
name  课程名字charfield  
desc  课程描述charfield
detail 课程详情textfield
degree 课程等级charfield choices max_length/default
learn_times 学习时长 integerfield default=0   #不懂
students 学习人数 integerfield default
fav_nums 收藏人数 integerfield default
iamge 图片 imagefield upload_to
click_nums 点击数 integerfield default
add_time 添加时间 datetimefield default=datetime.now

MeTa

```

3.
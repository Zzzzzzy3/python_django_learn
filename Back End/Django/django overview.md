## template

```python
先在app目录下创建templates

```
- 1.如果settings里面有join 先从根目录的templates里面找
- 2.根据APP的注册顺序去寻找文件
## static 静态文件
css和JavaScript 都必须在static目录中
```html
{% load static %}  
  
<!DOCTYPE html>  
<html lang="en">  
<head>  
    <meta charset="UTF-8">  
    <title>Title</title>  
    <link rel="stylesheet" href="{% static '/plugins/css/bootstrap.css' %}">  
</head>  
<body>  
<h1 class="container">用户列表</h1>  
  
<script src="{% static 'plugins/js/bootstrap.js' %}"></script>  
</body>  
</html>
```

## Django模板
在views里面
```python
def user_list(request):  
    name="zzy"  
    return render(request, '15.html',{'name1':name})  
    
def text(request):  
    data_list = [{"name": "zzy", "salary": 100000, "roles": "用户"},  
                 {"name": "zzy1", "salary": 100, "roles": "游客"},  
                 {"name": "zzy2", "salary": 10000, "roles": "管理员"}, ]  
    name = "zzy"  
    return render(request, 'user_list.html',{'n1': data_list,'n2': name})

```

# Django的ORM
```python
pip install mysqlclient
```
orm可以实现数据库表的增删查改
settings.py里面连接数据库
```
```
---
## django操作表
### 创建表
```python
from django.db import models  
  
# Create your models here.  
#创建表  
class Student(models.Model):  
    name = models.CharField(max_length=100)  
    age = models.IntegerField(max_length=100)  
    password = models.CharField(max_length=100)
    
#terminal里面输入
#python manage.py makemigrations
#python manage.py migrate

```
### 增删查改
```python
Department.objects.create(title="用户")  
Department.objects.create(title="工人")  
Department.objects.create(title="管理员")  
  
Student.objects.create(name="zzy",password="123",age="19")  
Department.objects.filter(id="1").delete()  
Department.objects.all().delete()  
  
data_list=Student.objects.all()  
for data in data_list:  
    print(data.name,data.password,data.age)  
    
row=Student.objects.filter(id=1).first  

Student.objects.all().update(age=18)

```

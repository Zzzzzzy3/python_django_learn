在虚拟环境下安装venv
```python
pip install django
```
-(在settings.py里面 删掉创建的templates)*不用了*


___

-![[Pasted image 20250322184718.png]]
- asgi.py和wsgi.py 用于接收网络请求(不需要管)
- **urls.py URL和函数的对应关系(经常使用)**
- **settings.py 项目配置(如MySQL连接)(经常修改)**
## APP
- APP指的是微服务
```
-项目
	-app,用户管理
	-app,订单管理
	-app,后台管理
	-app,网站
 ```
 ![[Pasted image 20250322185521.png]]
创建APP
 ```python
 python manage startapp app_name
```
注册app
```python
在settngs里面添加app_name.apps....config
```
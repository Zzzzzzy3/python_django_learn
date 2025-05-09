## 
### 创建表的操作
```c
creat table table_name{
	id int auto_increament primary key,
	name varchar(16),
	age int
}default charset=utf8;
```
### 删除表
```c
drop table table_name;
```
### 展示数据库下的表
```c
show tables;
```
### 展示表的结构
```c
desc table table_name;
```
### 常用的数据类型
- tinyint
	有符号 -128~127[默认]
	无符号0~255 使用unsigned
- int
	int 2*32*
	int unsigned 
- bignit
	bignit 2*64*
	bignit unsigned
- float
- double
- decimal 精度高于上面两
	`salary decimal(m,d) m是数字个数 d是小数点后个数` 
- char 定长字符串
	`salary char(10) `
- verchar 变长字符串
	有多长就给多长 char的查询速度快
- text
	text用于保存变长的大字符串 最大有6w个字符
- mediumtext  
- longtext 4GB左右
- datatime
	YYYY-MM-DD HH:mm:ss
- data
	YYYY-MM-DD
### 插入数据
```c
insert into table_name(salary,age) values(1000,19);
```
### 删除数据
```c
delete from table_name;
delete from table_name where condition;
```
### 查询数据
```c
select * from table_name;
select 列名,列名 from table_name where condition;
```
### 修改数据
```c
update table_name set 列=值 where condition;
```

## Python操作mysql
```python
pip install pymysql
```
### 连接使用msyql
```python
import pymysql  
  
while True:  
    sid = input("sid=")  
    if sid.upper() == 'Q':  
        break  
    name = input("name=")  
    age = input("age=")  
    time = input("time=")  
    shool = input("shool=")  
    # 连接Mysql  
    conn = pymysql.connect(host="127.0.0.1", port=3306, user="root", passwd="123456", db="testz", charset="utf8", )  
    cursor = conn.cursor(cursor=pymysql.cursors.DictCursor)  
    # 游标（cursor）是系统为用户开设的一个数据缓冲区，存放SQL语句的执行结果。每个游标区都有一个名字,用户可以用SQL语句逐一从游标中获取记录，并赋给主变量，交由主语言进一步处理。  
  
    # 发送数据  
    # cursor.execute("insert into student(sid,name,age,time,shool) values('3','xie','19','2022-04-04 00:00:00','jx')")  
  
    cursor.execute("insert into student(sid,name,age,time,shool) values(%s,%s,%s,%s,%s)")  
    cursor.execute(sql, [sid, name, age, time, shool])  
    conn.commit()  
    # 关闭  
    cursor.close()  
    conn.close()
```
注意不要用字符串格式化去做sql拼接,安全隐患SQL注入(在串中包含sql语法)
正确方法
```python
from flask import Flask, render_template, request  
import pymysql  
app = Flask(__name__)  
  
  
@app.route('/add/user', methods=['GET', 'POST'])  
def index():  
    if request.method == 'GET':  
        return render_template("add_user.html")  
    print(request.form)  
    username = request.form.get('user')  
    password = request.form.get('psw')  
    mobile = request.form.get('mobile')  
  
    #连接MySQL  
    conn = pymysql.connect(host="127.0.0.1", port=3306, user="root", passwd="123456", db="school", charset="utf8", )  
    cursor = conn.cursor(cursor=pymysql.cursors.DictCursor)  
    #执行SQL  
    cursor.execute("insert into user(username,password,mobile) values('%s','%s','%s')" % (username, password, mobile))  
    conn.commit()  
    #关闭SQL  
    cursor.close()  
  
  
    return "添加成功"  
  
  
if __name__ == '__main__':  
    app.run(debug=True)
```
___
### 查询
```python
import pymysql  
  
conn = pymysql.connect(host="127.0.0.1", port=3306, user="root", passwd="123456", db="testz", charset="utf8", )  
cursor = conn.cursor(cursor=pymysql.cursors.DictCursor)  
cursor.execute("select * from student where sid>%s",[2,])  
data_list=cursor.fetchall()#获取返回的值  
  
for data in data_list:  
    print(data)  
  
# 关闭  
cursor.close()  
conn.close()
```
### 删除
```python
import pymysql  
  
conn = pymysql.connect(host="127.0.0.1", port=3306, user="root", passwd="123456", db="testz", charset="utf8", )  
cursor = conn.cursor(cursor=pymysql.cursors.DictCursor)  
  
cursor.execute("delete from student where sid>%s",[2,])  
conn.commit()  
  
# 关闭  
cursor.close()  
conn.close()
```

修改
```python
import pymysql  
  
conn = pymysql.connect(host="127.0.0.1", port=3306, user="root", passwd="123456", db="testz", charset="utf8", )  
cursor = conn.cursor(cursor=pymysql.cursors.DictCursor)  
  
cursor.execute("update student set where sid=%s",[12,123])  
conn.commit()  
  
# 关闭  
cursor.close()  
conn.close()
```

在数据库中，将一个表中的所有记录复制到另一个表，可以通过 SQL 查询实现。具体的实现方式取决于两个表的结构是否完全相同，以及是否需要进行某些转换或过滤。

以下是几种常见的场景和实现方法：

### **场景 1：两个表结构完全相同**

如果目标表和源表的结构完全相同（字段名、字段类型、字段顺序都一致），可以直接使用 `INSERT INTO ... SELECT` 语句。

#### 示例：

假设你有两个表 `source_table` 和 `target_table`，它们的结构完全相同，你可以这样复制数据：


```sql
INSERT INTO target_table (column1, column2, column3)
SELECT column1, column2, column3
FROM source_table;
```

如果目标表和源表的字段顺序和名称完全一致，甚至可以省略字段名：


```sql
INSERT INTO target_table
SELECT * FROM source_table;
```
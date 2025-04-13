安装flask  `pip install flask` 
___
## flask框架
___

### `templates目录`
>templates应和py同一级目录
>flask框架自动打开templates文件

```python
from flask import Flask,render_template  
app = Flask(__name__)  
  
# 创建网址/show/info和index()对应关系  
# 访问show/info网址 自动执行index  
  
@app.route('/show/info')  
def index():  
    #return '中国联通'  
    return render_template("index.html")  
if __name__ == '__main__':  
    app.run(debug=True)
```

### `static目录`
```html
创建static目录 存放图片
<img src="/static/1.png" />
```

### Flask缺点
规定有些文件必须放在特定的文件夹
新创建一个页面


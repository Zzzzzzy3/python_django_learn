# 位置
1. 在css样式里面
2. html里面(推荐)
由于从上到下执行
3. 文件导入
```JavaScript
<script src="/"></script>
```
---
语法和C相似

# 1案例
![[Pasted image 20250320133457.png]]
```html
<!DOCTYPE html>  
<html lang="en">  
<head>  
    <meta charset="UTF-8">  
    <title>Title</title>  
</head>  
<body>  
<table border="1">  
    <thead>    <tr>        <th>ID</th>  
        <th>Name</th>  
        <th>SEX</th>  
    </tr>    </thead>    <tbody id="body">  
  
    </tbody>  
</table>  
<script type="text/javascript">  
    var data = [  
        {id: 1330, name: "zzy", age: 19},  
        {id: 1329, name: "zzy", age: 19},  
        {id: 1328, name: "zzy", age: 19},  
        {id: 1327, name: "zzy", age: 19}  
    ]  
    //  
    // var tr = document.createElement('tr'); tr行  
    //  
    for (var idx in data) {  
        text = data[idx];  
        var tr = document.createElement('tr');  
        for (var key in text) {  
  
            var td = document.createElement('td');  
            td.innerText = text[key];  
            tr.appendChild(td);  
        }  
        var bodyTag = document.getElementById("body");  
        bodyTag.appendChild(tr);  
    }  
  
  
</script>  
</body>  
</html>
```
# 函数
```JavaScript
function func(){  
      ;;;
}
```

# DOM
DOM,是一个模块,模块可以对HTML页面中的标签进行操作
```JavaScript
//根据ID获取标签
var tag=document.getElementById("xx");  

//获取标签中文本
tag.innerText  

//修改标签中的文本
tag.innerText="添加内容"

//创建标签<div>内容<div>
var tag = document.createElement('dib');
tag.innerText="内容"
```

添加
```JavaScript
<ul id="city">  
<!--    <li>北京</li>-->  
</ul>
  
var tag=document.getElementById("city");  
    var newtag=document.createElement("li");  
    newtag.innerText=("北京");  
    tag.appendChild(newtag);
```

绑定事件案例1
```JavaScript
<!DOCTYPE html>  
<html lang="en">  
<head>  
    <meta charset="UTF-8">  
    <title>Title</title>  
</head>  
<body>  
<input type="text" placeholder="请输入内容" id="txtuser">  
<input type="button" value="点击添加" onclick="addCity()">  
  
<ul id="city">  
    <!--    <li>北京</li>-->  
</ul>  
<script type="text/javascript">  
    function addCity() {  
        //定位输入标签  
        var txtTag = document.getElementById("txtuser");  
  
        //获取输入内容(value  
        var newstring = txtTag.value;  
  
        if(newstring.length>0) {  
  
            //创建标签  
            var newtag = document.createElement("li");  
            newtag.innerText = newstring;  
  
            //标签添加到ul中  
            var tag = document.getElementById("city");  
            tag.appendChild(newtag);  
  
            //将input框内容清空  
            txtTag.value = ""  
        }else{  
            alert("输入不能为空")  
        }  
    }  
</script>  
</body>  
</html>
```
---


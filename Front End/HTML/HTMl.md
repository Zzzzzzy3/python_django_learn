___
# 1.HTML认识
超文本传输语言

```html
<!DOCTYPE html>  
<html lang="en">  
<head>  
    <meta charset="UTF-8">  
    <title>Title</title>  
</head>  
<body>  
	
	
</body>  
</html>
```

## 1.1 `<div>`
	块级标签
## 1.2 `<span>`
	行内标签
	配合css
### 1.3 超链接
	跳转到其他 url 
	<a herl="">点击跳转</a>
跳转到自己网站`<a herl="/.">点击跳转</a>`
### 1.4 图片
```html
<img src="图片地址" />
```
	<img style="height: ;width: " src=" " />
	
	<a herl="" target="">
		<img scr="">
	</a>	
	
### 1.5 分类
分类(**块级标签和行内标签**)
-块级标签 #h1 #div #ul #ol
-行内标签 #span  #aherl #img 

### 1.6 #列表
```html
<ul>  
    <li>项目一</li>  
    <li>项目二</li>  
    <li>项目三</li>  
</ul>  
<ol>  
    <li>细则一</li>  
    <li>细则二</li>  
    <li>细则三</li>
</ol>
```
### 1.7 #表格
<table>  
    <thead>        <tr> <th>ID</th> <th>姓名</th> <th>年龄</th> </tr>  
    </thead>    <tbody>        <tr> <td>19</td> <td>zzy</td></tr>  
    </tbody></table>

### 1.8 #input系列
```html
<input type="text">  
<input type="password">  
<input type="file">  
<input type="checkbox">  
<input type="checkbox">  
<input type="checkbox">  
<input type="radio" name="n1">男  
<input type="radio" name="n1">女  
  
<input type="button" value="提交">  
<input type="submit" value="提交"> 提交表单
```

### 1.9 #下拉框
```html
<select>  
    <option>四川</option>  
    <option>成都</option>  
    <option>宜宾</option>  
</select>
```

### 1.10 #多行文本
```html
<textarea row="4"></textarea>
```
___
## URL
### 2.1 #GET请求 [URL请求]
	GET请求,跳转,向后台传入数据会拼接在URL上
	```
	(https://cn.bing.com/search?q=1&form=ANNTH1&refig=67cda4390221483aadb8157afc19e07f&pc=CNNDDB)
	```
### 2.2 #POST请求 [表单请求]
	提交的数据不在URl中,而是在请求体中
	
```html
<form method="post" action="/post/reg">

</form>
```

## 总结1
HTML标签与编程语言无关
pycharm可以快捷查看html在浏览器中,无需web框架

___

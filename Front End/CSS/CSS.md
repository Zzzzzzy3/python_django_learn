# CSS
## 3. #选择器

### ID选择器
```html
#c1{
}
```
### 类选择器
```html
.c1{
}
```
### 标签选择器
```html
li{
}

<li>....</li>
```
### 属性选择器
```html
input[type='text']{
	border:1px solid red;
}
```
### 后代选择器
```html
.(classname) c1{

} 
/*'>'作用是选择后代*/
.(classname) > a{

}

```

### #高度和宽度 
```html
<!DOCTYPE html>  
<html lang="en">  
<head>  
    <meta charset="UTF-8">  
    <title>Title</title>  
  <style>    .c1{  
      height: 300px;  
      width: 30%;  
    }  
  
  </style>  
  
</head>  
<body>  
<div class="c1">zzy</div>  
</body>  
</html>
```
高度不支持百分比
#### #块级和行内标签
CSS 
	改造行内标签 既具有行内标签和块级标签特性
```html
<!DOCTYPE html>  
<html lang="en">  
<head>  
    <meta charset="UTF-8">  
    <title>Title</title>  
  <style>    .c1{  
      display: inline-block;  
      color: red;  
      height: 100px;  
      width: 100px;  
      border: 1px solid gold;  
    }  
  
  </style>  
  
</head>  
<body>  
  <span class="c1">zzzzy</span>  
</body>  
</html>
```
inline行内 block块级*
___
块级+块级&行内
___
### #字体
```html
<!DOCTYPE html>  
<html lang="en">  
<head>  
    <meta charset="UTF-8">  
    <title>Title</title>  
  <style>    .c1{  
      color: gold;  
      font-size: 100px;  
      font-weight:500;  
      font-family: -apple-system;  
    }  
  
  </style>  
</head>  
<body>  
  <span class="c1">222sd</span>  
</body>  
</html>
```

### #浮动
```html
<span style="float: right">右边</span>
```

### #内边距
```html
<!DOCTYPE html>  
<html lang="en">  
<head>  
    <meta charset="UTF-8">  
    <title>Title</title>  
      <style>    .item{  
        float: left;  
        width: 400px;  
        height: 400px;  
        border: 1px solid gold;  
  
        padding-top: 20px;  
        padding-right: 20px;  
        padding-left: 20px;  
    }  
  
  </style>  
</head>  
<body>  
    <div class="item">  
        <div>            csgo  
        </div>  
    </div></body>  
</html>
```
padding: 上 右 下 左;

### 边距和居中案例
```html
<!DOCTYPE html>  
<html lang="en">  
<head>  
    <meta charset="UTF-8">  
    <title>Title</title>  
    <style>        body {  
            margin: 0;  
        }  
  
        .header {  
            height: 40px;  
            background-color: black;  
            margin-left: auto;  
            margin-right: auto;  
  
        }  
  
        .header .menu {  
            float: left;  
            color: darkgray;  
            height: 39px;  
            line-height: 39px;  
        }  
  
        .header .acocunt {  
            float: right;  
            color: darkgray;  
            height: 39px;  
            line-height: 39px;  
        }  
  
        .container {  
            width: 1226px;  
            margin: 0 auto;  
        }  
  
        .header a {  
            color: #fff;  
            position: relative;  
            height: 65px;  
           margin-left: 15px;  
        }  
  
  
    </style>  
</head>  
<body>  
<div class="header">  
    <div class="container">  
        <div class="menu">  
            <a>MIUI</a>  
            <a>Iot</a>  
            <a>开放平台</a>  
            <a>云服务</a>  
        </div>  
        <div class="acocunt">  
            <a>登录</a>  
            <a>注册</a>  
            <a>消息通知</a>  
        </div>
                <div style="clear: both"></div>  
    </div></div>  
</body>  
</html>
```

#文本居中
```html
<div style="width:200px; text-align:center;"
```

#区域居中
```html
.container{
	width:980px;
	margin:0 auto;
}
```

清除浮动
```html
 <div style="clear: both"></div>  
```

### 案例A1
```html
<!DOCTYPE html>  
<html lang="en">  
<head>  
    <meta charset="UTF-8">  
    <title>Title</title>  
    <style>        body {  
            margin: 0;  
        }  
/*第一部分 */        .sub-header {  
            height: 100px;  
            background-color: white;  
        }  
  
        .container {  
            width: 1128px;  
            height: 100px;  
            margin: 0 auto;  
  
        }  
  
        .sub-header .logo {  
            width: 234px;  
            height: 100px;  
            float: left;  
  
        }  
  
        .sub-header .menu-list {  
            width: 600px;  
            float: left;  
            height: 100px;  
            line-height: 100px;  
        }  
  
        .sub-header .menu-list a {  
            display: inline-block;  
            padding:0 20px;  
            color: #333;  
            height: 100px;  
            text-decoration: none;  
        }  
  
        .sub-header .menu-list a:hover{  
            color:#ff6700;  
        }  
  
        .sub-header .search {  
            width: 234px;  
            float: right;  
            height: 100px;  
        }  
/*第二部分 */        .header {  
            height: 40px;  
            background-color: black;  
            margin-left: auto;  
            margin-right: auto;  
  
        }  
  
        .header .menu {  
            float: left;  
            color: darkgray;  
            height: 39px;  
            line-height: 39px;  
        }  
  
        .header .menu a{  
            text-decoration: none;  
        }  
  
        .header .menu a:hover{  
            color: gold;  
        }  
  
        .header .acocunt {  
            float: right;  
            color: darkgray;  
            height: 39px;  
            line-height: 39px;  
        }  
  
        .container {  
            height: 100%;  
            width: 1226px;  
            margin: 0 auto;  
        }  
  
        .header a {  
            color: #fff;  
            position: relative;  
            height: 65px;  
           margin-left: 15px;  
        }  
/*第三部分 */        .slider .sd-img img{  
            width:100%;  
            height:100%;  
        }  
/*四*/  
  
      .news .channel{  
          width:228px;  
          height:170px;  
          background-color: #333;  
          padding: 3px;  
      }  
  
      .news .list-item img{  
          width: 316px;  
          height: 170px;  
      }  
      .news .channel .item{  
          height: 82px;  
          width: 75px;  
          float:left;  
          text-align: center;  
          padding-top: 18px;  
      }  
  
      .news .channel .item a{  
          font-size: 12px;  
          opacity: 0.7;  
          display: block;  
        padding-top: 18px;  
        text-overflow: ellipsis;  
        color: #fff;  
          text-decoration: none;  
      }  
  
      .news .channel .item img{  
          height:24px;  
          width: 24px;  
          display:block;  
          margin: 0 auto 4px;  
      }  
        .left{  
            float: left;  
        }  
  
  
    </style>  
  
</head>  
<body>  
<div class="header">  
    <div class="container">  
        <div class="menu">  
            <a href="https://www.mi.com">MIUI</a>  
            <a href="https://www.mi.com">Iot</a>  
            <a href="https://www.mi.com">开放平台</a>  
            <a href="https://www.mi.com">云服务</a>  
        </div>  
        <div class="acocunt">  
            <a>登录</a>  
            <a>注册</a>  
            <a>消息通知</a>  
        </div>        <div style="clear: both"></div>  
    </div></div>  
  
<div class="sub-header">  
    <div class="container">  
        <div class=" logo">  
            <a href="https://www.mi.com/shop" style="margin-top: 22px;display:inline-block">  
                <img src="https://cdn.cnbj1.fds.api.mi-img.com/mi.com-assets/shop/img/logo-mi2.png"  
                     style="height: 56px ;width: 56px;" alt="">  
            </a>        </div>        <div class="menu-list">  
            <a href="https://www.mi.com/shop">手机</a>  
            <a href="https://www.mi.com/shop">电脑</a>  
            <a href="https://www.mi.com/shop">手表</a>  
            <a href="https://www.mi.com/shop">服务</a>  
            <a href="https://www.mi.com/shop">小米商城</a>  
        </div>        <div class="search">  
  
        </div>        <div style="clear:both"></div>  
    </div></div>  
  
<div class="slider">  
    <div class="container">  
        <div class="sd-img">  
            <img src="https://cdn.cnbj1.fds.api.mi-img.com/mi-mall/2e389157059c44d9352b42e04407cbb7.jpg?w=2452&h=920" alt="no">  
        </div>    </div></div>  
  
<div class="news">  
    <div class="container ">  
        <div class="channel left">  
            <div class="item">  
                <a href="http://www.mi.com">  
                    <img src="https://cdn.cnbj1.fds.api.mi-img.com/mi-mall/82abdba456e8caaea5848a0cddce03db.png?w=48&h=48">  
                    保障服务  
                </a>  
            </div>            <div class="item">  
                 <a href="http://www.mi.com">  
                    <img src="https://cdn.cnbj1.fds.api.mi-img.com/mi-mall/82abdba456e8caaea5848a0cddce03db.png?w=48&h=48">  
                    保障服务  
                </a>  
            </div>            <div class="item">  
                <a href="http://www.mi.com">  
                    <img src="https://cdn.cnbj1.fds.api.mi-img.com/mi-mall/82abdba456e8caaea5848a0cddce03db.png?w=48&h=48">  
                    保障服务  
                </a>  
            </div>            <div class="item">  
                <a href="http://www.mi.com">  
                    <img src="https://cdn.cnbj1.fds.api.mi-img.com/mi-mall/82abdba456e8caaea5848a0cddce03db.png?w=48&h=48">  
                    保障服务  
                </a>  
            </div>            <div class="item">  
                <a href="http://www.mi.com">  
                    <img src="https://cdn.cnbj1.fds.api.mi-img.com/mi-mall/82abdba456e8caaea5848a0cddce03db.png?w=48&h=48">  
                    保障服务  
                </a>  
            </div>            <div class="item">  
                <a href="http://www.mi.com">  
                    <img src="https://cdn.cnbj1.fds.api.mi-img.com/mi-mall/82abdba456e8caaea5848a0cddce03db.png?w=48&h=48">  
                    保障服务  
                </a>  
            </div>        </div>        <div class="list-item left">  
            <img src="https://cdn.cnbj1.fds.api.mi-img.com/mi-mall/e981f78d2ac17c504975a719cb8b069d.png?w=632&h=340" alt="" style="margin-left: 14px">  
        </div>        <div class="list-item left">  
            <img src="https://cdn.cnbj1.fds.api.mi-img.com/mi-mall/6b04dfc206dec442fe161b33082681ec.png?w=632&h=340" alt=""style="margin-left: 14px"/>  
        </div>        <div class="list-item left">  
            <img src="https://cdn.cnbj1.fds.api.mi-img.com/mi-mall/6b0c7fadbd84a808287af5faad6e62d7.png?w=632&h=340" alt=""style="margin-left: 14px"/>  
        </div>        <div style="clear:both"></div>  
    </div>  
</div>  
</body>  
</html>
```
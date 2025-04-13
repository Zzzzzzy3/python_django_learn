# CSS
___
CCS专门用来美化标签
**层叠样式表**（Cascading Style Sheets，缩写为 **CSS**）是一种[样式表](https://developer.mozilla.org/zh-CN/docs/Web/API/StyleSheet)语言，用来描述 [HTML](https://developer.mozilla.org/zh-CN/docs/Web/HTML) 或 [XML](https://developer.mozilla.org/zh-CN/docs/Web/XML/Guides/XML_introduction)（包括如 [SVG](https://developer.mozilla.org/zh-CN/docs/Web/SVG)、[MathML](https://developer.mozilla.org/zh-CN/docs/Web/MathML) 或 [XHTML](https://developer.mozilla.org/zh-CN/docs/Glossary/XHTML) 之类的 XML 分支语言）文档的呈现方式。CSS 描述了在屏幕、纸质、音频等其他媒体上的元素应该如何被渲染的问题。

CSS 是**开放 Web** 的核心语言之一
___
## 1.在head标签中写 style 标签
```html
<head>  
    <meta charset="UTF-8">  
    <title>用户注册</title>  
    <style>        
	    .c1{  
            color:red;  
        }  
    </style>  
</head>
```
在需要渲染的元素前加入 class='name'

## 2.用link 导入
```html
<link rel="stylesheet" href="commen.css"/>
```
---

## 模板＋CSS+构建页面

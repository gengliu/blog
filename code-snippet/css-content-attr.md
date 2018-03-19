# 利用css的content属性attr抓取资料

```html
<div data-msg="Open this file in Github Desktop">  
hover
</div>
```

```css
div{
width:100px;
border:1px solid red;  
position:relative;
}
div:hover:after{
content:attr(data-msg);
position:absolute;
font-size: 12px;
width:200%;
line-height:30px;
text-align:center;
left:0;
top:25px;
border:1px solid green;
}
```



## 效果类似于

![attr](../assets/css-attr.jpg)
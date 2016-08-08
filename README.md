# Interview
个人面试总结
### 1，块级元素与行内元素有哪些，特点是什么？
```
块级：h div p 
行内：span a img input b i s

块级元素会独占一行,默认情况下,其宽度自动填满其父元素宽度. 　
块级元素可以设置width,height属性. 块级元素即使设置了宽度,仍然是独占一行.  块级元素可以设置margin和padding属性.　块级元素对应于display:block. 

行内元素不会独占一行,相邻的行内元素会排列在同一行里,
直到一行排不下,才会换行,其宽度随元素的内容而变化. 
行内元素设置width,height属性无效.
行内元素的margin和padding属性,水平方向的padding-left,padding-right,margin-left,margin-right都产生边距效果,
但竖直方向的padding-top,padding-bottom,margin-top,margin-bottom却不会产生边距效果.
行内元素对应于display:inline. 
```

### 2 什么是置换元素，包括哪些？
```
其中有类特殊的元素：如img|input|select|textarea|button|label等，他们被称为可置换元素（Replaced element）。
他们区别一般inline元素（相对而言，称non-replaced element）是：
这些元素拥有内在尺寸(intrinsic dimensions),他们可以设置width/height属性。
他们的性质同设置了display:inline-block的元素一致。
```
### 3 尺寸不固定， 实现图 边 里面还有个边？
```

```
### 4 百度图片搜索页面的布局原理？
```

```
### 5 css hack？
```
.element{
color:#000;             /*w3c标准*/
[;color:#f00;];         /*Webkit(chrome和safari)*/
color:#666\9;           /*IE8*/
*color:#999;            /*IE7 6*/
_color:#333;            /*IE6*/
}
:root .element{color:#0f0\9;}  /*IE9*/

@media all and (-webkit-min-device-pixel-ratio:10000), 
not all and (-webkit-min-device-pixel-ratio:0) { .element{color:#336699;}}  /*opera*/

@-moz-document url-prefix(){ .element{color:#f1f1f1;}} /*Firefox*/
```
### 6 未知宽高div居中？
```
/**主要代码*/
position:absolute;
top:50%;
left: 50%;
-webkit-transform: translate(-50%, -50%);
transform: translate(-50%, -50%);

/**主要代码*/
display: flex;
align-items: center;
justify-content: center;

/**主要代码*/
content:"";
display: inline-block;
vertical-align: middle;
height: 100%;
```
### 7 css3 z制作扇形？
```

```
### 8 看代码？
```
for(var i=1;i<=3;i++){
    setTimeout(function(){
        console.log(i);
    },0)
}
//3个4,注意i是4,但是循环了3回。
```

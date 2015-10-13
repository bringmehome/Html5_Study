#CSS3参考手册

>[CSS3背景](http://www.w3school.com.cn/css3/css3_background.asp)
>>图片自动撑满整个background，无叠加

**重要** <span style="color:red;">background-size需要写在background下面</span> **重要**

```js
    width: 300px;
    height: 300px;
    background:url(http://preview.quanjing.com/minden001/min143606.jpg);
    background-size:100px 100px;
    background-repeat:no-repeat;
    color: #FFF;
```

#[CSS3 3D 转换](http://www.w3school.com.cn/css3/css3_3dtransform.asp)

>拉伸
```js
#transitionid {
    width: 100px;
    height: 100px;
    background: green;
    transition: width 1s;
    color: white;
}
#transitionid:hover {
    width: 300px;
}
```

>将动画绑定到选择器
```js
#transitionid {
    width: 100px;
    height: 100px;
    background: green;
    transition: width 1s;
    color: white;
    animation: myfirst 5s;
}
@keyframes myfirst {
    width: 300px;
    from {
        background: red;
    }
    to {
        background: yellow;
    }
}
```

>当动画完成时，会变回初始的样式
```js
@keyframes myfirst {
    0%   {background:red;}
    25%  {background:yellow;}
    50%  {background:blue;}
    100% {background:black;}
}
```

>画正方形动作
```js
#transitionid {
    animation: myfirst 5s;
    position:relative;
}
@keyframes myfirst {
    0%   {background:red;left:0px; top:0px;}
    25%  {background:yellow; left:200px; top:0px;}
    50%  {background:blue;left:200px; top:200px;}
    75%  {background:gray;left: 0px; top: 200px}
    100% {background:black;left:0px; top:0px;}
}
```

>[CSS3 多列](http://www.w3school.com.cn/css3/css3_multiple_columns.asp)
```js
-webkit-column-rule:3px outset blue;
-webkit-column-count:2; /* Safari and Chrome */
column-gap:30px;
```

#[header](https://css-tricks.com/almanac/properties/d/display/)
>顶部header左右平分，并悬浮于页面

效果如下图<br/>
![](./img/zindexheader.png)<br/>

```js
.containers {
    width: 100%;
    display: flex;
    flex-flow: row wrap;
    text-align: center;
    padding: 10px 0;
    background: #EFF1F5;
    position: fixed;
    z-index: 9999;
}
.left {
    flex: 1;
    background: #ECBABA;
}
.main {
    width: 60%;
    background: #ACDCD0;
}
.right {
    flex: 2;
    background: #ECBABA;
}
```
```js
    <header class="containers">
        <div class="left">左</div>
        <div class="main">中</div>
        <div class="right">右</div>
    </header>
    <p style="height:700px;background:green;opacity: 0.4;"></p>
```


>justify-content的方式实现

效果如下图<br/>
![](./img/justify.png)<br/>

```js
#main {
  width: 400px;
  padding: 20px 0;
  border: 1px solid #c3c3c3;
  display: flex;
  justify-content: space-between; 
}
#main div {
  width: 70px;
  height: 70px;
}
```
```js
    <div id="main">
        <div style="background-color:coral;"></div>
        <div style="background-color:lightblue;"></div>
        <div style="background-color:khaki;"></div>
        <div style="background-color:pink;"></div>
    </div>
```

>垂直居中**align-items: center;**

效果如下图<br/>
![](./img/aligncenter.png)<br/>

```js
#main {
    width: 220px;
    height: 300px;
    border: 1px solid black;
    display: flex;
    align-items: center;
}
#main div {
    flex: 1;
}
```
```js
    <div id="main">
        <div style="background-color:coral;">红色</div>
        <div style="background-color:lightblue;">蓝色</div>
        <div style="background-color:lightgreen;">带有更多内容的绿色 div</div>
    </div>
```

>重写元素属性**align-self: center;**

效果如下图<br/>
![](./img/alignself.png)<br/>

```js
#main {
    width: 220px;
    height: 300px;
    border: 1px solid black;
    display: flex;
    align-items: flex-start;
}
#main div {
    flex: 1;
}
#myBlueDiv {
    align-self: center;
}
```
```js
    <div id="main">
        <div style="background-color:coral;">红色</div>
        <div style="background-color:lightblue;" id="myBlueDiv">蓝色</div>
        <div style="background-color:lightgreen;align-self: flex-end;">带有更多内容的绿色 div</div>
    </div>
    <p><b>注意：</b>align-self 属性可重写容器的 align-items 属性。</p>
```
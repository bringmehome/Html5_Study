#Html5的所有学习资料

>[JS正则](http://www.w3school.com.cn/js/js_obj_regexp.asp)
>>test()、exec() 以及 compile()

>[jQuery效果](http://www.w3school.com.cn/jquery/jquery_fade.asp)
>>隐藏或者显示
>>>hide(), show(), toggle()

>>淡入淡出
>>>fadeIn(), fadeOut(), fadeToggle()

>>滑动
>>>slideDown(), slideUp(), slideToggle()

>>动画
>>>animate()
```js
$("p").animate({
	left: '250px',
    opacity:'0.5',
    height: '+=150px',
    width: '+=150px',
}, 1000);
```

>>混合使用
```js
$("p").css("color","red").slideUp(1000).slideDown(1000);
```

>>元素之前或者之后插入
```js
$("p").prepend(" prepend ");
$("p").before(" before ");
$("p").after(" after ");
$("p").append(" append ");
```

>[设置CSS类](http://www.w3school.com.cn/jquery/jquery_css_classes.asp)
>>操作CSS
>>>addClass() - 向被选元素添加一个或多个类 
>>>removeClass() - 从被选元素删除一个或多个类 
>>>toggleClass() - 对被选元素进行添加/删除类的切换操作 
```js
$("p").addClass("testClass");
$("p").removeClass("testClass");
$("p").toggleClass("testClass");
```

>[遍历-过滤](http://www.w3school.com.cn/jquery/jquery_traversing_filtering.asp)
>>parent() 方法返回被选元素的直接父元素
>>parents() 方法返回被选元素的所有祖先元素，它一路向上直到文档的根元素 (<html>)
>>parentsUntil() 方法返回介于两个给定元素之间的所有祖先元素
>>children() 方法返回被选元素的所有直接子元素
>>find() 方法返回被选元素的后代元素，一路向下直到最后一个后代
>>siblings() 方法返回被选元素的所有同胞元素
>>next() 方法返回被选元素的下一个同胞元素
>>nextAll() 方法返回被选元素的所有跟随的同胞元素
>>nextUntil() 方法返回介于两个给定参数之间的所有跟随的同胞元素
>>prev(), prevAll() 以及 prevUntil() 方法的工作方式与上面的方法类似，只不过方向相反而已：它们返回的是前面的同胞元素（在 DOM 树中沿着同胞元素向后遍历，而不是向前）
>>first() 方法返回被选元素的首个元素
>>last() 方法返回被选元素的最后一个元素
>>eq() 方法返回被选元素中带有指定索引号的元素
>>filter() 方法允许您规定一个标准。不匹配这个标准的元素会被从集合中删除，匹配的元素会被返回
>>not() 方法返回不匹配标准的所有元素
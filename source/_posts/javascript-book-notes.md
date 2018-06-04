---
title: javascript高级程序设计笔记
date: 2018-05-08 11:12:06
categories:
- book
tags:
- javascript
---
#### 第五章 引用类型
1. 作为值得函数
*因为ECMAScript中的函数名本身就是变量，所以函数也可以作为值来使用。也就是说，不仅可以像传递参数一样把一个函数传给另个函数，而且可以将一个函数作为另个函数的结果返回。例子：*
```
	function callSomeFunction(someFunction,someArgument){
		return someFunction(someArgument);
	}
	function add10(num){
		return num+10;
	}
	var result1=callSomeFunction(add10,10);
	alert(result1); //20

	function getGreeting(name){
		return "Hello, "+name;
	}
	var result2=callSomeFunction(getGreeting,"Nicholas");
	alert(result2); //"Hello, Nicholas"
```

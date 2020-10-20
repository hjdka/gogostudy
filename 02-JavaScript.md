# JavaScript的用法

HTML 中的脚本必须位于 <script> 与 </script> 标签之间。

脚本可被放置在 HTML 页面的 <body> 和 <head> 部分中。

### head中

```
<script>
function myFunction()
{
    document.getElementById("demo").innerHTML="我的第一个 JavaScript 函数";
}
</script>
</head>
```

### html中

```
<html>
<body>
<p id="demo">一个段落</p>
<button type="button" onclick="myFunction()">尝试一下</button>
<script>
function myFunction()
{
    document.getElementById("demo").innerHTML="我的第一个 JavaScript 函数";
}
</script>
</body>
</html>
```

可以在 HTML 文档中放入不限数量的脚本。

脚本可位于 HTML 的 <body> 或 <head> 部分中，或者同时存在于两个部分中。

**通常的做法是把函数放入 <head> 部分中，或者放在页面底部**。这样就可以把它们安置到同一处位置，不会干扰页面的内容。



### 外部引入

```
<html>
<body>
<script src="myScript.js"></script>
</body>
</html>
```



# JavaScript 输出

## JavaScript 显示数据

JavaScript 可以通过不同的方式来输出数据：

- 使用 **window.alert()** 弹出警告框。



- 使用 **document.write()** 方法将内容写到 HTML 文档中。

  请使用 document.write() 仅仅向文档输出写内容。如果在文档已完成加载后执行 document.write，整个 HTML 页面将被覆盖。





- 使用 **console.log()** 写入到浏览器的控制台。

  ​

  **console.log()** 的用处

  主要是方便你调式javascript用的, 你可以看到你在页面中输出的内容。

  **相比alert他的优点是：**

  他能看到结构化的东西，如果是alert，弹出一个对象就是[object object],但是console能看到对象的内容。

  console不会打断你页面的操作，如果用alert弹出来内容，那么页面就死了，但是console输出内容后你页面还可以正常操作。






# JavaScript 语法



## JavaScript 字面量

在编程语言中，一般固定值称为字面量

**数字（Number）字面量** 可以是整数或者是小数，或者是科学计数(e)。

> 3.14
> 1001
> 123e5



**字符串（String）字面量** 可以使用单引号或双引号:

> "John Doe"
> 'John Doe'



**表达式字面量** 用于计算：

> 5 + 6
> 5 * 10



**数组（Array）字面量** 定义一个数组：

> [40, 100, 1, 5, 25, 10]、



对象（Object）字面量** 定义一个对象：

> {firstName:"John", lastName:"Doe", age:50, eyeColor:"blue"}



函数（Function）字面量** 定义一个函数：

> function myFunction(a, b) { return a * b;}
>
> 



## JavaScript 变量

在编程语言中，变量用于存储数据值。

JavaScript 使用关键字 **var** 来定义变量， 使用等号来为变量赋值

```
var x=4;
```



浏览器的组成?

​      外壳      = 地址栏  后  界面

​      内核     =  渲染引擎   html+css

​                  解析引擎   js



​     console 打印需要显示的内容   看是否是自己需要的数据



​    //  单行js注释

​    /*  多行js注释 */



# 笔记day1

## 输出方式

* console.log(1)  输出值,看看是否是自己需要的,

  alert()  

* 弹窗


* 打断程序的行



​	prompt()

* 弹窗输入


* 打断程序的进行




## 数据类型

  *   typeof	检测数据类型



  *   Number   数字类型     阿拉伯数字

  *   小数=浮点数  小数点后面

  *   尽快能不要使用浮点数,



  *   String   字符串类型  ""

  *   字符串类型 相加 +  是拼接的



  *   undefined  未定义类型



  *   null  空值类型



* Boolean  布尔类型  判断

  *   flase假      true真
  *   (0)
  *   (NAN)
  *   ("")
  *   (undefined)
  *   (null)
  *   (flase)
  *   ()
  *   {}  Object  对象
* []   Array 数组   数组是对象延伸的





```javascript
  var a = '1';

  console.log(typeof a);  // 字符串  Number

  var b = 1;

  console.log(typeof b);  // 数字  String

  var c;

  console.log(typeof c)   // 未定义类型  undefined

  var e = null;

  console.log(typeof e)   // 空值类型    object

  var f = Boolean(0)

  console.log(typeof f)   //布尔类型

  var obj  = {       // 对象写法

      0:b,

      1:9527,

      2:"你好",

      3:true,

      4:{

        5:"1111"

      }

  };

```



### 基础类型  

Number  string  Boolean  null  undefined

储存在 **栈区**

创建一个**变量** 会创一个**新的地址**,赋值那个地址



###  引用类型 

 Object Array function

储存在 **堆区**

创建一个变量会创一个新的地址 ,如果赋值的话是引用同一个内存地址



```javascript
  		//a接收        (页面显示)
        var a = prompt("你好,请输入数字")
        console.log(1-Number(a));  //
        Number(); //数字类型   转换成数字类型
        字符串转换成 数字
          // -  %  隐式的使用了进行转换成数字类型
        NaN //也是一种数字格式  是Number的旁类  就是计算不出的数字


   
```



##  获取DOM节点

   DOM    document object model 文档对象模型

​        

​         document.documentElement   获取html节点

​         document.head     获取head节点

​         document.body     获取body节点

​      

​        

 驼峰命名

​         document.getElementById("box") 获取的是单个id节点

1. ​	 document 文档
2. ​         get  获取
3. ​         Element  元素
4. ​         By   通过
5. ​         Id  什么选择器

​      

​         document.getElementsByClassName("选择器")  class 选择器  获取的是类数组 IE8以下不兼容

​         document.getElementsByTagName("")      标签选择器     获取的是类数组

​       

​       

##  innerHTML 操作元素节点属性

​          元素节点.inner HTML = "赋值"   替换原本节点的内容  ,能添加标签

​          元素节点.inner HTML就是获取元素内容,会获取的标签

​       

## intertext操作元素节点属性

​         元素节点.inner Text="赋值"    替换原本节点的内容  不能添加标签,把标签当做文本替换

​         元素节点.innerText   就是获取元素内容

​     

## 单双引号嵌套

​             "<p style=''>你好 世界</p>"

​         



元素.getAttribute("字符串")  // 获取

元素.setAttribute("属性名","设置属性值")		修改元素属性   行内

元素节点.removeAttribute("属性名") 		删除元素节点





```javascript
 		var aBox = document.getElementById("box");   // 所有兼容
		var  oBox1 =document.getElementsByClassName("box1");
		var  oBox2 =document.getElementsByTagName("div");  // 所有兼容
        
        // 获取节点
		var aB = document.querySelector("#box .box1")  // 获取单个    Ie7以下不兼
        var oB = document.querySelectorAll(".box1")  // 获取多个

        var aBox = document.getElementById("box");
        aBox.innerHTML = "<p style='font-size: 50px'>你好 世界</p>"
        var text = aBox.innerHTML
        aBox.innerText = "<p style='font-size: 50px'>你好 世界</p>"
        var ad =  aBox.getAttribute("name")   // 获取属性
        aBox.setAttribute("class","wrap")   //   设置属性
        aBox.setAttribute("style","font-size:50px;")   //   设置属性
        aBox.removeAttribute("class")   // 删除属性名
```



# day2

es6  字符串格式

``  字符串

 ${计算样式  变量 }

```javascript
var aBox =document.getElementById("box");
     aBox.innerHTML= `${num}元+666元=${num+666}元`
```



pageX=clientX+body.scrollLeft

pageY=clientY+body.scrollTop



# day3



 ## typeof 

是干嘛的?   检测数据类型

   Number()

   Number("")

   Number(null)

   Number([])

   Number(false) // 0

   Number(true)   //1

   Number({})    NaN

   Number([11])   // 11

  NaN == NaN   false

##    转换成字符串类型

​     ""  +  任何都会变成字符串

   String()  全局使用

​    .toString()   方法     不能转换 undefined null

  

##    作用域

?  指你有权访问的变量集合 ,函数

  

​     全局作用域 === window   window是一个对象

​     局部作用域 ===   函数内部

  

### 全局作用域  

网页或者script

​     在们打开页面的会创建一个 全局对象,关闭即销毁对象

​     在全局作用域创建的变量或者函数都会挂载带window身上,最大载体

​     全局作用域的变量,函数在任何作用域中都可以使用

  

### 局部作用域

  === 函数内部

调用函数的创建局部作用域,函数执行完毕就销毁,函数,变量也销毁,     

局部作用域的变量或函数,只能在函数内部使用,                                   除非使用闭包

每调用一次函数就会创建一个新的作用域,

  

局部作用域  就 是全局作用域的儿子

避免内存过多,

  

  

###    作用域查找

​       局部作用域自身没有,找上一级作用域,一直找到全局变量

​       局部作用域自身有那就使用自身的

  

   弱类型语音  尽可以能不会让你报错

  

###    IIFE  自执行函数   

自动执行,内部执行完毕销毁,执行一次

   (function(){})()   声明函数和调用为一体

​     不会污染全局变量函数命名冲突,

​     提升性能

  (function(){})()

  

  

   if esle 没有作用域的 所以外部是能获取到的

   for 没有作用域的

  

  

###    函数this指向对象

 	函数创建的时候  this就会指向一个对象

​	函数this默认指向window,除非调用时修改, 调用函数时this会改变指向

​	谁调用this执行就是谁

  

### 函数return值    返回值

​     返回return后面语句,代替原本的调用的位置

 	打断程序的进行不会执行后面的代码

  	相当于函数的结束

​	 用于节流



##   全局对象GO   局部AO对象



​     GO： 先进入全局作用域,找到所有变量和函数,赋值对应的初始值

​          	变量赋值undefined    函数赋值 function(){}

​          	解析一行,执行一行

​      AO：函数作用域

​        	1,每个进入函数就会创建一个AO对象

​        	2,找到所有的形参和变量,赋值初始值   undefined

​        	3,把所有实参赋值给形参,

​        	4,在函数内部找所有的函数声明,赋值  function(){}

​       		 5,解析一行,执行一行







## es6  变量声明

`et  const` 

 `var `  可以随便定义名称  除了关键字,保留字

  在用一个作用域中可以重复定义





###  let  

当做跟`var` 一样的就行  let就是声明变量

没有声明就不能使用

1. 能在同一个作用域  声明一样的名称,
2. 不会变量提升
3. 没有声明就使用,会触发 暂时性死区

```javascript
let a = 10;  a = 100;  console.log(a)
```



###  `const ` 

1. 只读不能修改
2. 不能在同一个作用域  声明一样的名称
3. 不会变量提升
4. 没有声明就使用,会触发 暂时性死区,



###  es6 和 es5  `var `变量的不同之处

es5 顶层对象是window和全局变量是一样的    全局变量挂载到window上面     变量 函数

es6  `let const`声明的全局变量不在属于顶层对象window , 在  script 上 ，还是全局属性

在全局创建的变量还是全局属性 只是挂载的地方不一样的  不可见,打印不出

 

```javascript
var a = 10;   
let c = 100;  
function f() {}
f();

   console.dir(c)
```

 

es5   没有块作用域

```javascript
  if(){var i = 0}    
     console.log(i);
 for(var i=0;i<5;i++){
   var a = 10;
 }
```



es6块作用域	声明的变量会有一个块作用域

```javascript
 {
let a = 0； //块作用域
}
```



 for循环的特殊性：可以将()当做{}父级作用域



# day4

## 字符串

1. 字符串拼接

``` charAt(index)```  index（下标值） 返回字符串下标对应值

```javascript
let str = 'ssddww'
let newStr = charAt(1)//s
let newStr = charAt(3)//d
```

``` charCodeAt(index)```  index （下标值）返回下标对应的`ascli` 码

```javascript
let str = 'ssddww'
let newStr = charCodeAt(1)//115
let newStr = charCodeAt(3)//100
```



``` String.fromCharCode(103)```  参数 ` ascll` 码  返回对应值

` str.indexOf(str[,num])`	 

- 参数 1= 需要查找的字符		
- 参数2 = 从索引位置开始查找
- 从字符串左到右查找，返回查找到对应下标，没有查到返回-1，只会找第一个。

` lastIndexOf(str[,num]) ` 

- 从右到左查找
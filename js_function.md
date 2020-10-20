####   题一 函数执行

​		

```js
//分别写出对fun两次调用alert的输出结果、井说明原理
function fun(a, b, c) {
      var l = arguments.length;
      var num = 0;
      for (var i = 0; i < l; i++) {
		num += arguments[i];
      }
      alert(num)
  } 
fun(1, 2, 3);    // 6
fun(1, 2, 3,4);   // 10

// 从上往下执行   
// arguments是什么?   传入的实参被接收存入到angunment类数组
```

#### 题二 函数执行

```javascript
//写出函数fun执行后console.log(a)的输出结果，并说明原理
 /*
* Go{
*    a=0
 *   fun=function
 * }
 * */
var a = 0;
function fun() {
       /*
        * AO{
        *   a=undefined
        *
        * }
        * */

    console.log(a)
    var a = 10
}
fun();
console.log(a)


//  变量声明 局部就是局部 全局就是全 
```

#### 题三  引用

```js
// 分别写出下面的执行 a 结果  及原理

//基础类型    栈区
var a = 0;
var b = a;
b++;
console.log(a)


//引用类型在 堆区
var o ={};
o.a = 0;
var c = o;
c.a = 10;
console.log(o.a)
```

#### 题四 函数执行

```js
// 分别写出下面的执行 a 结果  及原理
var a = 0;
function fun() {
    console.log(a);
    var a = 10;
    console.log(a);
}
fun();
console.log(a);
```

#### 题五 计算

```js
// 请分别计算 a 的值____   及类型                    
var a='abc'+123+456   

var a='456'-'123'   //  333   number
// * - % 都会隐式使用什么Number() 将字符串转换成数字类型

// 请计算c的值____
// 比较运算符  < > >=  <=  ==  !=  全部会类型转换
var a=1;
var b='2';
var c=a>b?(a<b?a:b):(a==b?a:b);  // "2"
```

#### 题六 循环/遍历

```js
// 打印 i  讲解其原理
for(var i=0;i<10;i++){
    console.log(i);  // 0
    break;    //  结束当前循环
}
console.log(i);  //  0
```

#### 题七 循环/遍历

```js
// 打印 i  讲解其原理
for(var i=0;i<10;i++){
    console.log(i);   //0-9
    continue;
}
console.log(i); // 10
```

#### 题八 this

```js
// 打印 json.val  讲解其原理
window.val=1; 
var json={ 
    val:10, 
    dbl:function(){ 
        this.val*=2; 
    } 
} 
json.dbl();  // 对象里面的
var dbl = json.dbl;  
dbl();   // 全距
console.log(json.val)

//函数创建的时候  this就会指向一个对象
//	函数this默认指向window,除非调用时修改, 调用函数时this会改变指向
//	谁调用函数this指向就是谁
```

#### 题九  this

```js
//  打印 console.log(json.val+val) 讲解其原理
(function(){
    var val =1;
    var json ={
          val:10,  // 属性名
          dbl:function(){
            val*=2;  // 变量
          }
    };
    json.dbl();
    console.log(json.val+val);   // 12
})();
```

#### 题十  函数执行

```js
// 打印执行结果  讲解其原理
var a=1;
var obj ={
"name":"tom"
}
function fn(){
    var a2 = a,
    obj2 = obj,
    a2 =a,
    obj2.name ="jack"
}
fn();
console.log(a);
console.log(obj);
```

#### 题十一  数组

```js
// 打印执行结果  讲解其原理
var ary =[1,4,3,2,6,5,8,7];
ary.push("666")
ary.pop()
ary.pop()
console.log(ary.join(""))
console.log(ary)
```

#### 题十二 字符串

​	

```js
// 打印执行结果  讲解其原理
var str ="123456789"
str.split("")
console.log(str)
console.log(str.split(""))
```

#### 题十三 数组

```
数组的pop()、push()、shift()、unshift()分别是什么？
```

#### 题十四 闭包

```
闭包，作用是什么?

	是一个函数可以把自己内部的语句和自身所声明时所在的作用域形成一个密封的环境,
      在函数外部可以读取到函数内部的变量和函数,函数内部的变量会被保存下来,不会被回收,闭包不会被销毁,
```

#### 题十五  Number

```js
// 打印执行结果  讲解其原理
var num="abc123";
num=parseInt(num);
if(num==123){
   alert(123);
}else if(num===NaN){
   alert(NaN);
}else if(typeof num=="number"){
   alert("number")
}else{
   alert("str");
}
```

#### 题十六  比较

```
js中的==和===作用
1=="1"   true
1==="1"  false
```

#### 题十七  数组

```
什么是类数组
一定会有具有length长度
没有数组的方法
```

#### 题十八   闭包

```js
// // 打印执行结果  讲解其原理
function fn(i) {
   return function (n) {
         console.log(n + i++)
   }
}
var f = fn(10)
f(20)   
fn(20)(40)
fn(30)(50) 
f(30) 

// ++在后 在先计算在赋值      不参与运算
// ++在前  先加赋值在计算     参与运算
```

#### 题十九 节点

```
怎么添加、移除、复制、创建、和查找节点
```






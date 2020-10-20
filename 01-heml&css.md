# day1

## 标签语义化

<h1> 网页最大标题 只能写一个

​		提高网页的排名 写在log下面

h2-h6   内容标题 可以随便多写

​    		从大到小的写


<div>     容器可以装任何东西

<p>       包裹一段文字
<span>    包裹重要文字

<img>     引入图片

​	属性    src  图片地址

​	alt  图片描述 图片未引用成功时显示在页面ali中描述内容

​	title   当鼠标移到到标签时显示内容

​	在哪里引入图片就在哪里开始找

## 相对路径

  ./同级文件    
  /打开文件夹
  ../打开上一级
​    <!--./1.jpg -->

<dl>  <dt> <dd>

## 对话列表

dl

    dt 标题
    dd 内容



# day2

## 列表

<ul><li>      无序列表

css样式
list-style：none 去除列表圆点或排序

​        	   disc    默认实心圆
​       		   circle  空心圆
​        	   square  黑心方块


<ol> <li>      有序列表

设置<ol>列表
type=""         阿拉伯（1）/字母（a/A）/罗马数字（I/i）



## <a>标签   

超链接  跳转网页的      需要载体
href="网页地址/路径（自己设置的地址）"
target=""  

​            _blank  点击一次打开一个网页
​            _new    只打开一个（乱写效果一样）
​            _self   默认设置        只在当前网页打开新的页面
​            
​            不跳转网页
​			href="#" 
​			href="javascript:void(0)"   




## 锚点

        从一个地方 自动到另外一个地方
        方法一
                <a href="#move">1</a>  点击位置        href="#名称"
                <a href="" name="move"></a>   跳转位置  name="名称"
        方法二
                <a href="#move">1</a>  点击位置        href="#名称"
                id="名称"



## css

div  标签===元素

css操作 ==> 页面的装饰，修饰，布局，  

怎么写css样式

选择器  是很么给元素取名

行内样式 在标签的旁边

  第一个位置
  css写的位置  内联样式 

head > style > css样


  名字是规范的:不能以数字开头,不要大写小写字母,不要特殊符合,拼音

​    正常的规范:语义化

### 企业命名规范参考文件

#### (一)网页内容类                                                  

标题: title

摘要:summary

箭头： arrow

商标： label

网站标志： logo

转角/圆角： corner

横幅广告：banner

子菜单： subMenu

搜索：search

搜索框：searchBox

登录： login

登录条：loginbar

工具条：toolbar

下拉：drop

标签页：tab

当前的：current

列表：list

滚动：scroll

服务： service

提示信息：msg

热点：hot

新闻： news

小技巧：tips

下载： download

栏目标题： title

热点：hot

加入：joinus

注册：regsiter

指南：guide

友情链接： friendlink

状态： status

版权： copyright

按钮： btn

合作伙伴：partner

投票：vote

左右中：leftright center

 

#### (二)注释的写法:

 

/*Footer */

内容区

/*End Footer */

 

#### (三)id的命名:

 

##### (1)页面结构

 

容器:container

页头：header

内容：content/container

页面主体：main

页尾：footer

导航：nav

侧栏：sidebar

栏目：column

页面外围控制整体布局宽度：wrapper

左右中：leftright center

 

##### (2)导航

 

导航：nav

主导航：mainnav

子导航：subnav

顶导航：topnav

边导航：sidebar

左导航：leftsidebar

右导航：rightsidebar

菜单：menu

子菜单：submenu

标题:title

摘要:summary

 

##### (3)功能

 

标志：logo

广告：banner

登陆：login

登录条：loginbar

注册：regsiter

搜索：search

功能区：shop

标题：title

加入：joinus

状态：status

按钮：btn

滚动：scroll

标签页：tab

文章列表：list

提示信息：msg

当前的:current

小技巧：tips

图标:icon

注释：note

指南：guild

服务：service

热点：hot

新闻：news

下载：download

投票：vote

合作伙伴：partner

友情链接：link

版权：copyright

 

#### (四)class的命名:

 

##### (1)颜色

使用颜色的名称或者16进制代码,如

.red{ color: red; }

.f60{ color: #f60; }

.ff8600{ color: #ff8600; }

##### (2)字体大小

直接使用"font+字体大小"作为名称,如

.font12px{ font-size: 12px; }

.font9pt{font-size: 9pt; }

##### (3)对齐样式

使用对齐目标的英文名称,如

.left{ float:left; }

.bottom{ float:bottom; }

 

##### (4)标题栏样式

使用"类别+功能"的方式命名,如

.barnews{ }

.barproduct{ }

 

#### 注意事项

1.一律小写;

2.尽量用英文;

3.不加中杠和下划线;

4.尽量不缩写，除非一看就明白的单词.

 

#### 推荐的CSS 书写顺序

//显示属性

display

list-style

position

float

clear

//自身属性

width

height

margin

padding

border

background

//文本属性

color

font

text-decoration

text-align

vertical-align

white-space

othertext

content





##   id选择器   

      id="名字"              一个元素只能取一个id名,  id是唯一的,
                          一个页面不要设置太多的id名,权重问题,5-10;          
      以#开头  + 名字  { }

##   class选择器

    class="名字"      一个元素可以取多个,可以随便使用,
    以.开头 + 名字 { }   

  >   子级 空格 后代选择器 

（+）相邻选择器

通过邻居选择自己

 （~） 兄弟选择器

  只有是兄弟就通过它选择到自己

（*）全部选择中  任何元素生效样式

  标签选择器  元素<div> <p>

  权重的问题
 1000分  100    10      1 
行内> id > class > 标签 >  * 

条件==:当同一种选择器选到一个元素的时候

 后写覆盖前面的
就近原则

## css位置写法

  行内样式 >  内联  >  外联

外联 ==  工作  实战
link rel=""  href="路径"
<link rel="stylesheet" href="./t.css">
stylesheet  css样式表



# day3

## css样式（部分）

opacity:元素透明  0-1;    还是会存在页面中  只是透明

background  元素背景   颜色

### 单位（部分）

px 	像素

em   1em==自身元素字体大小  2*字体大小

rem    html的字体大小  html有默认的字体大小 16px

​        1rem =16px  默认值 

vh      视口的高度 分100份     1vh = 视口的高度/100    自动计算出来的

vw      视口的宽度 分100份    1vw  = 视口的宽度 / 100



### 文字样式（部分）

行高:   行内元素自动垂直居中  浏览器自动计算

 line-height:   元素垂直居中 设置要包裹文字元素的高度

####  文字水平对齐  

 text-align: center      文字居中

​	            	left        左对齐

​			 right       右对齐

​                	justify      两端对齐   

font-size 	字体大小

color     		字体颜色

font-weight  	字体加粗  100-900 

​              		bold 加粗

font-style: italic  字体倾斜

font-family: "微软雅黑";   系统配置的

text-indent: 2em;  首行字母缩进

text-decoration:   none;   去除划线

​                  		underline        添加下划线

​                 		line-through    添加贯穿线

​                  		overline        添加上划线

#### 垂直对齐

行内元素就是以基线对齐   

基线中文是看不出的  英文字母才能好看出

baseline默认基线在 x的双脚下面



vertical-align ：baseline；

​			baseline：使元素的基线与父元素的基线对齐

​			middle：使元素的中部与父元素的中线对齐

​			top：使元素及其后代元素的顶部与整行的顶部对齐

​			bottom：使元素及其后代元素的底部与整行的底部对齐。

#### 引入自定义字体

@font-face{

  font-family: "字体名称";

  src: url("路径");

} 





### 鼠标样式    

当鼠标移动到设置元素上改变鼠标图标

cursor: pointer;

​      		auto  默认。浏览器设置的光标。

​    	  	crosshair 光标呈现为十字线。

​     		 pointer 光标呈现为指示链接的指针（一只手）

​      		move  此光标指示某对象可被移动。

​     		 text  此光标指示文本。

​     		 wait  此光标指示程序正忙（通常是一只表或沙漏）。

​     		 help  此光标指示可用的帮助（通常是一个问号或一个气球）

## 标准盒模型

 外边距    内边距  边框     主体内容

 margin  padding  border  content 

​    

###  主体内容 

 content= width + height  

 页面元素显示的大小

 元素宽 =   width + 左右padding +  左右border

 元素高 =   height + 上下padding + 上下border



### 边框     

复合属性

####     第一种写法 

​         /* 宽度  属性     颜色*/

```
  border:10px  solid  green; 
```

​                  solid   实线

​                  dashed  虚线

​                  double  双横线

​                  dotted   圆点线

####     第二种写法

```
border-width:2px 2px 20px 2px;         
```

​     			上  右  下  左

​                    	上  左右  下

​                    	上下  左右

​                    	全部

```
border-style: solid dashed dotted double;
```

​                    	上  右  下  左

​                    	上   左右  下

​                   	上下  左右

​                   	 全部

```
border-color: pink  red  green yellow;
```

​                    	上  右  下  左

​                    	上  左右  下

​                    	上下  左右

​                    	全部

####       第三种写法

​       

```
 border: 2px solid green;
```

```
 border-width: 2px 2px 20px 2px    
```

​        			左边  右边  上边 下边

​        			left right top  bottom

```
 border-left:10px   solid  green
```

颜色透明

​    transparent

### 外边距

  margin 

 两个盒子之间的间隙,无论父子,还是兄弟

####  外边距合并问题

#####   父子外边距

  1,给父级设置边框

  2,给父级设置内边距

##### 兄弟外边距

====>>避免就好了,

  盒子外边距垂直相对,

   		两值为正,  生效最大值

   		 一正一负,  相加的结果值

​    		两值为负    重叠

### 内边距

 padding 

位置 ===  边框和主体内容之间

设置内边距 元素会变大,

 复合属性  

 padding:20px  20px 20px 20px;

​            	上  右  下  左

​            	上  左右  下

​            	上下  左右

​            	全部

​    左边  右边  上边 下边

​    left right top  bottom

​    padding-left:10px   

​    背景颜色padding 是没有自身的颜色, 元素背景是怎么样 ==它就是怎样的,

​    设置padding的时候 就理解为在元素的那个方向,插入一点空白

## 怪异盒模型  

开启

```
 box-sizing:border-box；
```

 margin  padding  border  content 

  

  元素设置的宽度是多少就是多少====页面元素宽

  元素设置的高度是多少就是多少====页面元素高

  设置的padding 或者 border 会自动剪切宽或者高



# day4

##  块元素 

```
display:block;
```

​    块元素       	   行内元素       行内块元素

​    块级盒模型    行内盒模型   行内块盒模型



块元素==块级盒模型,  <div><p>< h1~h6> <ul><li>  <ol><li>  <form> 

 特性

​	1,独占一行

  	2,宽度不写,默认继承父级100%宽度

  	3,高度不写,有里面的内容撑开高度,

 	4,支持margin padding auto   水平居中

​	5,p标签不可包裹块级元素(只存放文本)

## 行内元素   

```
display:inline;
```

行内元素==行内盒模型，   <a> <b> <i> <span> 

 特性

​	1,和其他的行内元素并排在一行;

 	2,不支持margin-top bottom 支持左右;支持padding    

 	3,不支持宽高

​	4.a标签能包裹块级元素(特殊,区域链接)

​	5,标签之间的空格解析

注意：浏览器在解析行内元素的时候会将空格解析成显示在页面的空格,   解析成一个

解决方法:

  	1, 删除空格

 	 2, 给父级设置字体大小为零, 如果文字不见,重新设置文字大小就行. 



## 行内块   

```
display:inline-block;
```

行内块==行内块盒模型  <img>	<input>

 特性

​	1,支持宽高

​	2,支持margin padding

​	3,本质上还是行内元素,只是具有了块元素的特性

​	4,<img>标签不是行内块元素(是行内元素,但是可以设置宽高，这源自于历史…)

## 类型转换

  	可以把行内元素转换成  块元素,行内块元素,

  	块元素   ===>         行内元素, 行内块元素;

 	 行内块元素  ====>    行内元素,块元素

想要谁改变就设置谁的css样式--display;



## 元素的显示与隐藏

```
display：none；
```

隐藏对象: 		

display: block有显示的意义,和display: none;隐藏不显示	

特点: 	

1. 不占据空间（如同消失一般）,无法点击交互	
  2. 内部子元素也不会显示
2. display为none的元素浏览器不会渲染



元素从页面中消失  

```
display:none 
```

  

元素显示  display:block   会具有对应的特性

​            	 inline

​            	 inline-block

# day5

## css选择器。

伪类选择器 :hover   当鼠标移动到元素上是生效:hover后面的css样式

通过选择器:hover

```
  .box:hover{}
```



## 替换元素

非替换元素：指内容可以直接在代码中写出来（如文字）

替换元素：是指内容存储在代码文件之外，需要通过文件路径引入（如图片，视频，音频等）

1.替换元素是浏览器根据其标签的元素与属性来判断显示具体的内容。img、input、textarea、select、object 等都是替换元素，这些元素都没有实际的内容。

2.替换元素可以增加行框高度，但不增加line-height，内容区高度值 = padding-top + padding-bottom + margin-top + margin-bottom + height。

3.要想替换元素居中，可以设置line-height = height， vertical-align = middle



## 文字样式（补）

### 文字换行

​    white-space: normal;  默认文本换行

​               		 nowrap;   文本不换行

​              

超出元素隐藏

​    overflow:hidden;  

文本出现滚动

​    overflow:scroll; 文本出现滚动条

​    overflow:auto;   文本一旦超出元素就出现滚动条,

​                      		没有超出就不出现  



### 本出现省略号      

三合一  缺一不可

​    white-space: nowrap;  文本不换行

​    overflow:hidden; 

​    text-overflow:ellipse

英文字符换行  数字

  word-break: break-all;

/* 不能选中文字 */

user-select: none;

/* 字体间隙 */

letter-spacing: 10px;





# day6

## 背景

### background 元素背景  

​    background-color: green;          背景颜色

​    background-image: url("路径"); 引入背景图片

​    background-repeat: no-repeat;     去除平铺

​                       			repeat-x       x轴平铺

​                      			 repeat-y       y轴平铺

background-position: 100px 100px; 背景图片位置

​                         		x      y

​    					left right top bottom  center

background-size: 700px  500px ;背景图片的大小

​                      		宽     	高

​                		cover    放大背景图片到整个元素的大小

​               			 contain  等比例放大，  有一条边触碰到元素的界限，就会停止放大

​                	颜色  	图片    	平铺    		位置     		大小

background：color	 image 	repeat 	position	 /	 size

```
 background: url("./0.jpg")   left top  / 200px 200px  no-repeat,
      green url("./0.jpg") no-repeat    right  bottom  / 200px 200px 
      ;
```

 

​    元素的层级

​      边框|内容 >  背景图片 > 背景颜色



### 颜色rgba属性



​      

###    背景 css3 属性

​        origin 图片的起始位置

​            content-box  主体内容开始

​            padding-box   内边距位置开始

​            border-box    边框位置开始

​        clip   背景剪切

​            content-box  主体内容 背景剪切

​            padding-box   内边距位置 背景剪切

​            border-box    边框位置 背景剪切

/* 背景图片依附  */

​      background-attachment: fixed; 背景图片不跟随元素滚动，固定位置  

​                            scroll  跟随元素滚动

## 圆角

border-radius:8px;

​    左上 右上 右下  左下    

​    左上 右上左下  右下                          

​    左上右下  右上左下

​    全部                              

​                     

border-top-left-radius:左上

border-top-right-radius:右上

border-bottom-right-radius:右下

border-bottom-left-radius:左下





# day7



## 浮动



flot：left；

​	right

浮动和display:inline-block的区别

​      1,display会有空格 ,   浮动没有空格

​      2,display不能控制方向, 浮动能控制方向的,

​      3,没有基线对齐问题,    浮动没有基线问题.

基线对齐问题解决 

​    vertical-align:top

​    以前浮动用于图文布局



## 文档流

float:left

  什么是什么文档流?   普通文档流===标准文档流  在第0层

​    就是页面的布局,从页面的左上角开始,   

  1 2 3 4 5 6 7 8 

  浮动定义:

​    遇到父元素或者相邻的浮动元素,会让浮动元素停止在当前位置,

​    如果上一个元素是普通文档流元素,那么这个浮动元素相对垂直位置不变,

​    相邻的浮动元素会并排成一行,

  特性

​    1,能控制方向,

​    2,相邻的浮动元素会并排成一行,父级宽不够会被挤到下一行

​    3,浮动会改变元素的类型block,

​    4,文字能感受浮动的位置,

  设置了浮动元素的  半脱离文档流   飘到 1.5层 全部在1.5





## 浮动引起的高度塌陷问题

浮动会造成附近高度塌陷,

  块元素不设置高度,飞起来了没东西撑开,

  怎么解决?

  1, 设置高度

  2, overflow:hidden;    触发一个机制,bfc的机制,     Block Formatting Context

​                      给元素添加一个虚拟容器,肉眼是看不见的,浏览器能感受到,

​                      容器不影响容器外面的布局,外面的布局不会影响里面.

​      display:inline-block;

​      float:left;

​      position:absolute;

  3,利用一个幽灵元素来清除浮动，手动撑开父元素的高度;

​    伪元素选择器来做?

  ::before                                                                                                                             

  ::after	伪元素选择器     做装饰

  ::before    正文之前    是一个行内元素

  ::after     正文之后

  激活?

​    content:" "   激活使用  写了就能激活



  

.wrap::after{

  content: "";

  display: block;

  width: 0;

  height: 0;

  clear: both;

}

  怎么清除浮动?

  clear:left  左     左边不能有浮动元素,自己到下一行去     只能清除设置左浮动的元素

​       right  右                                        只能清除设置右浮动的元素

​       both   两边   只能设置浮动元素的元素

浮动元素会被卡主





# day8



定位

position

## 相对定位

定位   position:relative;    相对定位

​    位置 = 参照物 = 自身的初始设置位置   

​    特性

​      1,不会脱离文档流,但是会飘起来,

​      2,占据元素初始位置

​      3,支持margin

​      4,不会影响的类型,不会影响我们的布局

​      5，可随意移动方向



##     绝对定位

​    定位  position;absolute;    

​    位置  = 参照物  = 根据祖先是否有定位样式来进行定位,如果祖先没有定位样式会根据浏览器的窗口来定位

​      定位样式

​        position:relative;

​        position;absolute;

​        position:fixed;

​    特性:

​      1,完全脱离文档流,不会保留初始位置,

​      2,会转换元素的类型  block

​      3,支持margin      auto暂时失效

​      4,父相子绝,

​      5,html结构 后写居上

​      6,根据祖先是否有定位样式来进行定位,如果祖先没有定位样式会根据浏览器的窗口来定位



## 固定定位

​    position:fixed;  

​    位置  = 参照物  = 浏览器的窗口=== 可以见区域的窗口定位

​    1,完全脱离文档流,不会保留初始位置

​    2,以窗口定位,不会跟随浏览器窗口 滚动而滚动





  position:static 什么都没有 就是文档流该怎么样 就怎么样



 定位中  以left 和 top为尊

​        left  right  只生效left

​        top   bottom 只生效 top

​        解决

​      还原默认值

​      auto



## 移动属性

​    left  right  top  bottom

​    文档流  =  半脱离文档流  = 完全脱离文档流



## 层级问题

​    z-index: 数字  默认值  auto 

​    数字越大 越在上面  

​    数字越小 越在下面  

  层级比较问题

​      是兄弟层级的比较

  z-index只能生效  relative  absolute  fixed 定位样式







% ：FF(完全不透明)
10% ：E5
20% ：CC
30% ：B2
40% ：99
50% ：7F
60% ：66
70% ：4C
80% ：33
90% ：19
100% ：00(全透明)
16进制透明度



# day9

## 渐变

就是 图片的替代品,  消耗性能

渐变 是css写的 

渐变:  有两种或者两种以上颜色组成,

### 线向渐变

 一把刷子   

​                      to 控制方向    从后面读取

 linear-gradient(to top,    red , green ,yellow);

​                      deg  角度度

控制方向 left right top bottom              

​                      一般使用px 

​   平铺

 repeating-linear-gradient(  to 控制方向 ,颜色)

###  径向渐变    

从中心位置向四周扩撒

  圆  circle               

​                            at  x  y

​    radial-gradient(circle at 50% 50%,red , green)

​    椭圆                    	     宽       高

 radial-gradient(ellipse  100px  100px at 50% 50%,red , green)

默认是farthest-corner          

  closest-side:半径为从圆心到最近边 

  closest-corner:半径为从圆心到最近角 

  farthest-side:半径为从圆心到最远边 

​	  farthest-side:半径为从圆心到最远角 

  

background-image: radial-gradient(closest-side circle at top left ,red,blue);





# day10

## 表单

form  表单  登录页面   提交的时候会刷新页面   ajax 不会刷新页面

action="向服务器发送数据的地址"

name="名称"  被id选择器代替

id=""  id选择器  权重问题 

method="发送数据的方式"

​            get      get  发送数据不安全     

​            post     post 相对安全



```
  <form action="https://www.baidu.com/"  id="form" method="GET"></form>
```



## input 控件

行内块元素 

### 属性

​      type 控件的类型

​      name 名称

​      value  控件的初始值

​      placeholder  控件的输入提示

​      autocomplete 是否记录提交过的内容  off 不记忆  on记忆 

​      autofocus   光标自动聚焦

​      required     必须填写



### type类型

​      text      文本输入框

​      password  密码输入框

​      submit    提交按钮

​      reset     重置按钮

​      radio   单选   需要添加name值一致 不添加浏览器不会认为是一类的

​      checkbox 多选   disabled 禁止勾选

​                      checked   默认勾选中

​      file   文件    multiple 上传多个文件   accept=".jpg,.html" 限制上传文件 

​      image  图片

​      email  邮箱 

​                     

去除input的默认样式

 outline:none  边框光标



css3类型    

​      number  数字输入框  min最小值  max 最大值  小数 不推荐使用  js不支持小数

​      range   数字滑块    min最小值  max 最大值  

​      time     时间

​      date     年月日

​      week     年周

​      color    颜色

​      month    年月



## 伪类选择器

​    hover     当鼠标移动元素上时生效

​    focus          鼠标聚焦在输入框中是生效

​    focus-within:  鼠标聚焦在后代或自身输入框中时生效

​    placeholder     修改提升提示字体样式

​    checkbox   勾选时触发样式



# day11

## 浏览器渲染原理

 hmlt + css

​        浏览器渲染元素

​        1,读取html结构,生成一个DOM树

​        2,读取css规则,生成一个css规则树

​        3,合并DOM树,css规则树生成  render树    计算布局      重排

​        4,生成页面,渲染生成                                  重绘

​        读取html = > 样式 =>渲染





## 选择器   

​        id

​        标签

​        class

​        ~  兄弟

​        +  相邻

​        ,  并集

​        >  子带

​        空格   后代

​        .  交集

​        *  通配符

### 伪类选择器

​        :hover  鼠标移动到元素生效

​        :checKed   被勾选时触发css样式

​        :focus   鼠标聚焦时生效

​        :focus-within  自身或者后代的时候鼠标聚焦生效

​        ::placeholder   input的提示设置样式

​        :not()      反选

  	

​    

​     标签或者class类名  :not("选择器")    反选

​       not(这么输入的选择器 不会被选中,其他的会选中) 

   

​    a标签 没有被点击过 就是蓝色

​        开始     蓝色     link

​        点击     变红     active

​        点击之后 紫色     visited

​	:active  点击时候的生效

​        

::before  正文之前添加

 ::after   正文之后添加

​    激活content=""   行内    

​    除了添加文字  还能再里面添加其他元素?  div

能干嘛的?

   装饰的, 里面不会再有内容,

存在的意思

​        装饰的,

​        给文本添加内容



不是所有的元素都有伪元素?

img input  单标签没有伪元素 

​    

​    ::first-line 改变首行样式

​    :first-letter 改变首个文字样式

​    ::selection   改变选中的文字颜色

### 结构性伪类选择器

​        第一种写法

​            e=元素   e:nth-child(n)  n=第几个  

​            选中e元素父级的所有子集中的第n个  

​        第二种写法

​            奇数      1 3 5 7 9

​            偶数      2 4 6 8 10            

​            nth-child(odd)   

​                odd  奇数  

​                even 偶数

​        第三种写法

​            e:nth-child(n+2)  n+2     从第二个开始全部选择到后面的e元素

​                    -n+3  -n+3    倒着来数

​        e:nth-of-type(n)       

​        选中e元素父级的所有子集中的第n个  无视其他不是e元素  

​        

​        e:first-child

​        选中e元素父级的所有子集中的第一个 

​        e:last-child

​        选中e元素父级的所有子集中的最后一个 

###   属性选择器

​       div[class="box"]  

​       ^    以什么开始 div[class^="1"]

​       *    包含什么   div[class*="1"]

​       \$     以什么结束 div[class$="1"]





# 表格

table

 大标题

​       caption  标题

​        tr  行

​        td th 列    行和列交叉 就是单元格

​        th  标题  自动居中

​        td  内容  

/* 合并单元格 */

​    border-collapse: collapse;

/* 单元格间隙 */

border-spacing: 20px;

​    合并单元格

​    条件:    colspan="n"  n表示几   行合并单元格

​            要先删除一个才能合并,

​     

​            rowspan="n"       列

可写可不写

​    <thead></thead>   表头

​    <tbody></tbody>   内容主体

​    <tfoot></tfoot>   表尾

​        





# day12



##     过渡效果  

伪类选择器做   复合属性从开始没有时间 瞬间到达  有时间过渡效果

transition:属性  时间  贝赛尔曲线  延时

transition-property:属性  width  height left top等  all全部的属性  控制那个属性变化

​            -duration:时间

​            -timing-function: 贝赛尔曲线;    运动轨迹

​                             linear 匀速运动

​                             ease   默认 先慢 在快  在慢 

​                             ease-in  匀加速

​                             ease-out 匀减速

​                             ease-in-out 先加速 在减速

​        贝赛尔曲线:https://cubic-bezier.com/  网址 cubic-bezier(.12,-0.46,.4,1.52)

​        x轴 = 时间

​        y轴 = 距离

​            delay: 延时   正数要延迟  负数提前

​    

​    效果

​     起始位置

​     终点位置

​     时间

​    被动   浏览器上怎么触发的   用鼠标去触发效果



## 动画

animation

被动动画   起点  终点 时间

主动动画   浏览器自动执行的动画

​     animation:动画名 时间  曲线  延时 执行方向 播放次数 停止位置 

​     animation-name:动画名 

​           -duration：时间

​           -timing-function：贝赛尔曲线

​           -delay：延时

​           -iteration-count：播放次数   infinite  无限次数

​           -direction: reverse;  反方向

​                    		alternate  默认方向来回  默认是设置的方向  1 3 5 7 9 设置方向 2 4 6 8 10 反方向

​                    		alternate-reverse 反方向来回

​    动画停止

​        通过被动触发停止 :hover  :active 

​    /* paused 停止动画 running 默认值 运动 */

​        animation-play-state: paused; 停止动画

​    动画运动完毕停止位置   前提条件是什么?  不能设置动画执行次数是 infinite无数次

​    /* 动画停止位置 backwards  开始位置   forwards结束位置*/

​    animation-fill-mode: forwards;



关键帧

​        aniamtion-timing-function: steps()  

```
 /* 制作关键帧 keyframes   名称 */
        @keyframes move {
            /* 起点位置 */
            form{
                left: 0;
            }
            /* 终点位置 */
            to{
                left: 1000px;
            }
        }
```



百分比

```
  /* 制作关键帧 keyframes   名称 */
        @keyframes move {
            0%{
                left: 0;
                top: 0;
                background: red;
            }
            25%{
                left: 1000px;
                top: 0;
                background: green;
                border: 20px solid red;

            }
            50%{
                left: 1000px;
                top: 700px; 
                background: pink;

            }
            75%{
                left: 0px;
                top: 700px;
                background: yellow;

            }
            100%{
                left: 0;
                top: 0; 
                background: red;
                animation: name duration timing-function delay iteration-count direction fill-mode;
            }
        }
```





## day13

## 元素位置变换

 transform 操作元素的平移/translate  缩放/scale  倾斜/skew 旋转/rotate  操作原点/transform-origin

​        复合属性

transform: translate(100px,200px); 

​        平移   x      y   

​            translate(100px,200px)

​            translate(x)

​            translateX()   x

​            translateY()   y

​            translateZ()   z   

​            以四条边定位

​        缩放    元素所有全部会跟着缩放

​        scale(1.5)  放大

​        scale(.5)   缩小   

​        scale(1,2) scale(宽,高)

​        scale(-2)  负数=倒立

​                原心位置  在中心位置

​        倾斜skew()

​            skew(45deg)  x轴

​            skew(45deg,60deg) x  y

​            skewX()

​            skewY()

​        原心位置  在中心位置

​        旋转rotate(45deg)

​            rotate(45deg)  z轴

​            rotateX()

​            rotateY()

​        旋转圆心位置在中心

​                                 x     y

​        transform-origin;    10px 10px

​                            left top right bottom  center  100%;

​            设置 圆心位置  

​        修改元素圆心的样式    

​            scale()

​            skew()

​            rotate()



## 优化

 transform和position:relative 

position:relative 

​        不会脱离文档流,占据初始位置     重排

transform

​        不会脱离文档流,占据初始位置     重绘

动画性能优化的区别; 如果说不是动画性能优化 基本差别不大,





浏览器的渲染原理,

​        1,读取html结构,生成一个DOM树

​        2,读取css规则,生成一个css规则树

​        3,合并DOM树,css规则树生成  render树    计算布局      重排; 

​        4,生成页面,渲染生成                                 重绘

​        读取html = > 样式 => 渲染



## 2D转3D

 站在远处才能知道是3D

​    要设置在站远处观看   才能看出近大远小的效果

x y z

景视

```
 perspective: 700px;
```



## 阴影

```
box-shadow：xOffset yOffset burlLehgth spread color outset;
盒阴影:水平方向偏移 垂直方向偏移 阴影模糊距离 阴影缩放 阴影颜色 阴影显示方式；

```

## 滤镜

```

filter: url("filters.svg#filter-id");

/* <filter-function> values */
filter: blur(5px);	设置高斯模糊
filter: brightness(0.4);  0-1变暗 最低编程黑色，大于1 越来越亮 最高变成透明 。
filter: contrast(200%);#调整图像的对比度，值是0%的话，图像会全黑。值是100%，图像不变。值可以超过100%，意味着会运用更低的对比。若没有设置值，默认是1
filter: drop-shadow(16px 16px 20px blue);
阴影效果：<offset-x> <offset-y> <blur-radius>/值越大，越模糊，则阴影会变得更大更淡.不允许负值 若未设定，默认是0 (则阴影的边界很锐利)<spread-radius>/阴影扩张和变大，负值会是阴影缩小 <color> 
filter: grayscale(50%);灰度图像
filter: hue-rotate(90deg);给图像应用色相旋转
filter: invert(75%);反转输入图像
filter: opacity(25%);转化图像的透明程度
filter: saturate(30%);转换图像饱和度
filter: sepia(60%);将图像转换为深褐色

/* Multiple filters */
filter: contrast(175%) brightness(3%);

```



# day14



## 弹性布局

display;flex;



 标准盒模型 

​            宽度不设置,默认继承父级的宽度,

​            高度不写,由内容撑开,

 display: flex; 开始弹性盒模型;

​           父级控制子级; 

### 特点

​           1,会将所有子元素并排成一行,自动分配空间

​           2,宽度不设置,内容撑开,

​           3,高度不写,默认继承父级的高度.

​     元素在浏览器显示的宽度,      直接检测盒模型

​     求的是单个的=元素设置的宽度/一行子元素宽之和*父元素的宽度

 

### 控制主轴的方向

​        flex-direction: row;   默认方向   从左往右

​                     row-reverse         从右往左

​                     column              从上往下

​                     column-reverse      从下往上

### 交叉轴换行    

​        换行是有条件的,子元素宽度之和大于父元素宽度

​        flex-wrap:wrap                    向下换行

​                nowrap                   不换行

​                wrap-reverse              向上换行

​    复合写法

​        flex-flow:主轴  交叉轴;



### 主轴多行样式对齐

​        justify-content:flex-start;  起点位置对齐

​                        flex-end     终点位置对齐

​                        center       居中对齐

​                        space-between            

​        两端对齐,子元素与子元素之间留有空隙

​                        space-around

​        父子之间有空隙,子元素与子元素之间留有空隙

​                        space-evenly

​        父子之间的空隙===子元素与子元素之间留有空隙

​        父子之间的空隙和子元素与子元素之是一样的



### 交叉轴多行样式样式



#### 交叉轴多行样式

​        align-content:主轴多行样式一样;

#### 交叉轴单行样式

​        align-items:flex-start;  起点位置对齐

​                    flex-end     终点位置对齐

​                    center       居中对齐

​                    baseline     基线对齐

​        写在子元素里面 

#### 交叉轴单个样式

​        align-self:flex-start;  起点位置对齐

​                    	flex-end     终点位置对齐

​                    	center       居中对齐

### 弹性布局  排版

​        order:0  默认值 

​    数字越小元素排在越前

​    数字越大元素排在越后

​    

### 弹性增长因子

​     条件一行元素宽度之和要小于父元素宽度才会生效

​        flex-grow:0   默认值

​    一行中如果有增长因子 ,会让元素将所以间隙占据,

​    可以设置多个           按间隙比例放大

 元素1的实际 =  元素1的宽度(100px) + (父元素宽度-子元素之和)*元素1的弹性增长因子/子元素弹性因子和  

​              

### 缩小因子

​        条件一行元素宽度之和要 大于父元素宽度才会生效

​        flex-shrink:1  默认值1 

  会将元素缩小

一行元素中 设置大于1   会将元素缩小,其他放大   按比例  

元素1的实际=元素1的宽度(150px)-(子元素宽之和一父元素宽度)缩放因子之和

​    flex:auto   一行有剩余就扩大  没有就缩小

​    flex:none   设置多少就是多少

# diy15

## 网格布局

display：grid

父级控制子级

## 特性：

- 继承父级宽度100%，高度自动分配


- 开启 display ：block
- 只对子级生效



## 容器属性1



水平就是行，垂直就是列

grid-template-columns：；

grid-template-rows：；

单位 	px		百分比

简便写法 1：

避免输入重复单位

repeat（4，20%）两个参数

​	重复次数	，宽度/高度



简便写法 2：

repeat（auto-fill，100px）

自动填满容器元素



简便写法3：

fr单位 去除不是fr 单位的长高  剩下的长高 / fr相加的数值=1fr

剩余空间 比列分配、

简便写法4：

auto 浏览器自动分配 



## 容器属性2



grid-row-gap：；行间隙

grid-column-gap：；列间隙

grid-gap：行间隙 列间隙；



## 容器属性3

 父：grid-template-areas：`a b c`

​				`d e f`

​				`g h i`;

子：grid-area：a；



## 容器属性4

排版布局

grid-auto-flow：row/column；

​			行/列



## 容器布局5






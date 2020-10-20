# apache安装配置
## 安装
> 安装路径D:\wamp
## 配置根路径
> 默认的网站根路径是安装目录的www子目录（D:\wamp\www），如果不想使用默认目录，可以自己配置。配置方式如下：

- 找到文件D:\wamp\bin\apache\Apache2.4.4\conf\httpd.conf 或者打开如下文件（实际是同一个文件）
   <br>![](./img/2.png)
- 在文件中搜索DocumentRoot，找到239行位置
- 修改根路径为如下形式：(如果要配置虚拟主机，这里配置成根路径；如果不配置根路径，可以配置成D:\ajax；现在配置的是虚拟主机形式；两个位置应该保持一致)
   <br>![](./img/1.png)

## 配置虚拟主机
> 配置虚拟主机可以配置多个网站（域名和网站目录对应），配置步骤如下

- 开启虚拟主机辅配置，在httpd.conf 中找到如下位置,然后把前面的井号去掉
  <br>![](./img/3.png)
- 配置虚拟主机，打开conf/extra/httpd-vhosts.conf
  <br>![](./img/4.png)
  <br>分别修改以下三项，其它项无需指定。
    + DocumentRoot "E:/www/example"
    + ServerName "example.com "
    + ServerAlias "www.example.com"
- 修改DNS（hosts）文件(C:\Windows\System32\drivers\etc\hosts),
  添加如下内容：<br>
  127.0.0.1  example.com  <br>
  127.0.0.1  www.example.com
- 重启apache
- 访问http://www.example.com或者http://example.com
## 配置多个虚拟主机的实例如下：
- httpd-vhosts.conf文件配置
  <br>![](./img/5.png)
- hosts文件配置
  <br>![](./img/6.png)




# 原生Ajax

## 四部曲

```javascript
			//1. 创建XMLHttpRequest
                var xhr = new XMLHttpRequest();
                // 2.准备发送
                xhr.open('get', './check.php?username=' + uname + '&password=' + pw, true)
                //3. 执行发送动作
                xhr.send(null);
                // 4.指定回调函数
                xhr.onreadystatechange = function () {
                    if (xhr.readyState == 4) {
                        if (xhr.status == 200) {
                            var data = xhr.responseText;
                            var info = document.getElementById('info');
                            if (data == '1') {
                                info.innerHTML = 'success!'
                            } else if (data == '2') {
                                info.innerHTML = 'debate';
                            }
                        }
                    }
                }
```



```JavaScript
 btn.onclick = function () {
                var uname = document.getElementById('username').value;
                var pw = document.getElementById('password').value;
                // 创建XMLHttpRequest
                var xht = null;
                if(window.XMLHttpRequest){
                    var xhr = new XMLHttpRequest(); //标准
                }else{
                    var xhr = new ActiveXObject('Microsoft.XMLHTTP');   //IE6
                }

                //readyState == 0       表示xhr对象初始化完成
               
                //准备发送
                /* 
                    参数一：请求方式（get获取数据，post提交数据）
                    参数儿：请求地址
                    参数三：同步或异步标准位，默认true异步，false同步  

                    用send发送数据 必须设置请求头   setRequestHeader           
                 */

                var param = 'username=' + uname + '&password=' + pw;
                xhr.open('post', 'post.php', true);
                
                //执行发生动作

                xhr.setRequestHeader("Content-type",'application/x-www-form-urlencoded')
                xhr.send(param); //post请求参数在这传递 ，并且不需要转码
            
                 //readyState == 1      表示已经发送请求
               
                //指定回调函数
                //该函数调用条件readyState状态发生变化(不包括0-1)
               xhr.onreadystatechange=function(){  
                   /* 
                   readyState:
                   2    浏览器已经收到服务器响应的数据
                   3    正在解析数据
                   4    数据已经解析完成，可以使用了，但数据不一定是正确的
                    */
                   if(xhr.readyState == 4){
                       if(xhr.status == 200){
                          /* 
                         http 常见状态码
                           200 表示数据正常 响应成功
                           404 没找到请求资源
                           500 服务器端错误
                            */
                           alert(xhr.responseText);
                       }
                   }
               }
            }
```



# Json

json数据和普通的js对象区别：

1. json数据没有变量
2. json形式的数据结尾没有分号
3. 接送数据中的键必须用双引号包住

## json数据解析

` var data = JOSN.parse(d)`		json数据格式转化为js对象

` var s=JOSN.stringify(obj)`		对象转化为字符串

` var a = eval("("+data+)")`			eval字符串转化为js代码并执行	早期使用/安全隐患



# jQuery中ajax使用



```javascript
$.ajax({
  type:'get',
  url:'./1.php',
  data:{code:code},
  dataType:'json',
  success:function(data){
  }
});
```

```javascript
$(function(){
  $("#btn").click(function(){
    var code = $("#3code").val();
    $.ajax({
      typr:'get',
      url:'1.php',
      data:{code:code},
      dataType:'json',
      success:function(data){
        if(data.falg == 0){
          $("#info").html("sssss");
        }else{
          var tag="ssss";
          $("#info")=tag;
        }
      }
      error:function(data){
      console.log(data);
    }
    })
  })
})
```
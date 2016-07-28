
前言
----

怎样学习http


HTTP协议处理流程
-----------------

我们平时在浏览网页的时候都是使用浏览器，输入你要的网址后回车，就会显示出我们所想要的内容，看似这个简单的用户操作行为的背后，Web的工作原理是怎样的呢？到底隐藏了些什么呢？

对于传统的上网流程，系统它是这么做的：浏览器本身它是一个客户端，当输入URL地址的时候，浏览器首先会去请求DNS服务器，通过DNS查询获取相应的域名所对应的IP地址，然后通过这个映射的IP地址找到IP对应的服务器，并建立连接，等浏览器发送完HTTP Request（请求）包后，服务器接收到请求包之后才开始处理，返回HTTP Response（响应）包，客户端浏览器收到来自服务器的响应后就开始渲染这个Response包里的主体（body）部分，等收到全部的内容后断开与该服务器之间的连接。

一个Web服务器也被称为HTTP服务器，它通过HTTP协议与客户端通信。这个客户端通常指的是Web浏览器(其实手机端客户端内部也是浏览器实现的)。

Web服务器的工作原理可以简单地定义为：
1. 客户机通过TCP/IP协议建立到服务器的TCP连接
2. 客户端向服务器发送HTTP协议请求包，请求服务器里的资源文档
3. 服务器向客户机发送HTTP协议应答包，如果请求的资源包含有动态语言的内容，那么服务器会调用动态语言的解释引擎负责处理“动态内容”，并将处理得到的数据返回给客户端
4. 客户机与服务器断开。由客户端解释HTML文档，在客户端屏幕上渲染图形结果

一个简单的HTTP事务就是这样实现的，看起来很复杂，原理其实是挺简单的。需要注意的是客户机与服务器之间的通信是非持久连接的，也就是当服务器发送了应答后就与客户机断开连接，等待下一次请求。

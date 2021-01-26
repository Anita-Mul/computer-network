## 2.1 HTTP协议用于客户端和服务器之间的通信
  - 请求访问文本或图像等资源的一端称为`客户端`，而提供资源响应的一端称为`服务器端`。
  - 在两台计算机之间使用HTTP协议通信时，在一条通信线路上必定有一端是客户端，另一端则是服务器端。
  - 两台计算机作为客户端和服务器端的角色有可能会互换。但就仅从一条通信路线来说，服务器端和客户端的角色是确定的，而用HTTP协议能够明确区分哪端是客户端，哪端是服务器端。


## 2.2 通过请求和响应交换达成通信
 - 肯定是先从客户端开始建立通信的，服务器端在没有接收到请求之前不会发送响应。
![在这里插入图片描述](httpsimg-blog.csdnimg.cn20210126112017423.pngx-oss-process=imagewatermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0FuaXRhU3Vu,size_16,color_FFFFFF,t_70)
![在这里插入图片描述](httpsimg-blog.csdnimg.cn20210126112132531.png)
 - GET：表示请求访问服务器的类型
 - index.html：指明了请求访问的资源对象（请求URI）
 - HTTP1.1：HTTP的版本号，用来提示客户端使用的HTTP协议功能。

请求报文是由请求方法、请求URI、协议版本、可选的请求首部字段和内容实体构成的。
![在这里插入图片描述](httpsimg-blog.csdnimg.cn20210126112416111.pngx-oss-process=imagewatermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0FuaXRhU3Vu,size_16,color_FFFFFF,t_70)
——————
![在这里插入图片描述](httpsimg-blog.csdnimg.cn20210126112534655.pngx-oss-process=imagewatermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0FuaXRhU3Vu,size_16,color_FFFFFF,t_70)
 - HTTP1.1：表示服务器对应的HTTP版本
 - 200 OK：表示请求的处理结果的状态码（statuscode）和原因短语（reason-phrase）
 - Data：创建响应的日期时间

![在这里插入图片描述](httpsimg-blog.csdnimg.cn20210126112821294.pngx-oss-process=imagewatermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0FuaXRhU3Vu,size_16,color_FFFFFF,t_70)

## 2.3 HTTP是不保存状态的协议
 - 在HTTP这个级别，协议对于发送过的请求或响应都不做持久化处理
![在这里插入图片描述](httpsimg-blog.csdnimg.cn20210126113008287.pngx-oss-process=imagewatermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0FuaXRhU3Vu,size_16,color_FFFFFF,t_70)
 - 使用HTTP协议，每当有新的请求发送时，就会有对应的新响应产生。
 - HTTP1.1虽然是无状态协议，但为了实现期望的保持状态功能，于是引入了Cookie技术

## 2.4 请求URI定位资源
 - HTTP协议使用URI定位互联网上的资源
 - 指定请求URI的方式：
	![在这里插入图片描述](httpsimg-blog.csdnimg.cn20210126113353706.pngx-oss-process=imagewatermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0FuaXRhU3Vu,size_16,color_FFFFFF,t_70)
 - 如果不是访问特定资源而是对服务器本身发起请求，可以用一个来代替请求URI。下面这个例子是查询HTTP服务器端支持的HTTP方法种类。
	![在这里插入图片描述](httpsimg-blog.csdnimg.cn20210126113500343.png)

## 2.5 告知服务器意图的HTTP方法
HTTP1.1 中可使用的方法：

#### GET：获取资源
 - GET方法用来请求访问已被URI识别的资源。指定的资源经服务器端解析后返回响应内容
 - 如果请求的资源是文本，那就保持原样返回；如果是像CGI（Common GatewayInterface，通用网关接口）那样的程序，则返回经过执行后的输出结果。
![在这里插入图片描述](httpsimg-blog.csdnimg.cn20210126113938945.pngx-oss-process=imagewatermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0FuaXRhU3Vu,size_16,color_FFFFFF,t_70)
#### POST：传输实体主体
 - 虽然用GET方法也可以传输实体的主体，但一般不用GET方法进行传输，而是用POST方法
![在这里插入图片描述](httpsimg-blog.csdnimg.cn20210126114548361.png)
#### PUT：传输文件
 - 要求在请求报文的主体中包含文件内容，然后保存到请求URI指定的位置。
 - 鉴于HTTP1.1的PUT方法自身不带验证机制，任何人都可以上传文件，存在安全性问题，因此一般的Web网站不使用该方法
![在这里插入图片描述](httpsimg-blog.csdnimg.cn20210126115148147.pngx-oss-process=imagewatermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0FuaXRhU3Vu,size_16,color_FFFFFF,t_70)
#### HEAD：获得报文首部
 - HEAD方法和GET方法一样，只是不返回报文主体部分。用于确认URI的有效性及资源更新的日期时间等。
![在这里插入图片描述](httpsimg-blog.csdnimg.cn20210126115622954.png)
#### DELETE：删除文件
 - HTTP1.1的DELETE方法本身和PUT方法一样不带验证机制，所以一般的Web网站也不使用DELETE方法。当配合Web应用程序的验证机制，或遵守REST标准时还是有可能会开放使用的。
![在这里插入图片描述](httpsimg-blog.csdnimg.cn20210126115807349.png)
#### OPTIONS：询问支持的方法
 - OPTIONS方法用来查询针对请求URI指定的资源支持的方法。
![在这里插入图片描述](httpsimg-blog.csdnimg.cn20210126135745995.png)
#### TRACE：追踪路径
 - TRACE方法是让Web服务器端将之前的请求通信环回给客户端的方法。
 - 发送请求时，在Max-Forwards首部字段中填入数值，每经过一个服务器端就将该数字减1，当数值刚好减到0时，就停止继续传输，最后接收到请求的服务器端则返回状态码200 OK的响应。
 - TRACE方法本来就不怎么常用，再加上它容易引发XST（Cross-Site Tracing，跨站追踪）攻击，通常就更不会用到了。
![在这里插入图片描述](httpsimg-blog.csdnimg.cn20210126140242475.png)
## CONNECT：要求用隧道协议连接代理
 - CONNECT方法要求在与代理服务器通信时建立隧道，实现用隧道协议进行TCP通信。主要使用SSL（Secure SocketsLayer，安全套接层）和TLS（Transport Layer Security，传输层安全）协议把通信内容加密后经网络隧道传输。
![在这里插入图片描述](httpsimg-blog.csdnimg.cn20210126140341338.png)

## 2.6 使用方法下达命令
 - 方法：可以指定请求的资源按期望产生某种行为。方法中有GET、POST和HEAD等。
![在这里插入图片描述](httpsimg-blog.csdnimg.cn20210126140756117.pngx-oss-process=imagewatermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0FuaXRhU3Vu,size_16,color_FFFFFF,t_70)

## 2.7 持久连接节省通信量
 - HTTP协议的初始版本中，每进行一次HTTP通信就要断开一次TCP连接。
![在这里插入图片描述](httpsimg-blog.csdnimg.cn20210126141028873.pngx-oss-process=imagewatermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0FuaXRhU3Vu,size_16,color_FFFFFF,t_70)
如果发送一份包含多张图片的HTML文档，会产生大量的通信开销

#### 2.7.1 持久连接
 - 只要任意一端没有明确提出断开连接，则保持TCP连接状态。（HTTP1.1和一部分的HTTP1.0）
	![在这里插入图片描述](httpsimg-blog.csdnimg.cn20210126141546325.pngx-oss-process=imagewatermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0FuaXRhU3Vu,size_16,color_FFFFFF,t_70)
#### 2.7.2 管线化
 - 管线化技术出现后，不用等待响应亦可直接发送下一个请求。
 ![在这里插入图片描述](httpsimg-blog.csdnimg.cn20210126141959481.pngx-oss-process=imagewatermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0FuaXRhU3Vu,size_16,color_FFFFFF,t_70)

## 2.8 使用Cookie的状态管理
 - HTTP是无状态协议，它不对之前发生过的请求和响应的状态进行管理
 - Cookie技术通过在请求和响应报文中写入Cookie信息来控制客户端的状态。
![在这里插入图片描述](httpsimg-blog.csdnimg.cn2021012614254550.pngx-oss-process=imagewatermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0FuaXRhU3Vu,size_16,color_FFFFFF,t_70)
![在这里插入图片描述](httpsimg-blog.csdnimg.cn20210126142652500.pngx-oss-![在这里插入图片描述](httpsimg-blog.csdnimg.cn20210126142709362.pngx-oss-process=imagewatermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0FuaXRhU3Vu,size_16,color_FFFFFF,t_70)
![在这里插入图片描述](httpsimg-blog.csdnimg.cn20210126142725264.pngx-oss-process=imagewatermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0FuaXRhU3Vu,size_16,color_FFFFFF,t_70)

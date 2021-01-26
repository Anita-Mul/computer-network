#### 1.1 使用HTTP协议访问Web
![在这里插入图片描述](https://img-blog.csdnimg.cn/2021012608505885.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0FuaXRhU3Vu,size_16,color_FFFFFF,t_70)
![在这里插入图片描述](https://img-blog.csdnimg.cn/20210126085212652.png)
 - Web使用一种名为HTTP（HyperText Transfer Protocol，超文本传输协议[插图]）的协议作为规范，完成从客户端到服务器端等一系列运作流程
 - Web是建立在HTTP协议上通信的。

#### 1.2 HTTP的诞生 
 - 为知识共享而规划Web
 - 1997年1月公布的HTTP/1.1是目前主流的HTTP协议版本
 - 当年HTTP协议的出现主要是为了解决文本传输的难题。由于协议本身非常简单，于是在此基础上设想了很多应用方法并投入了实际使用


#### 1.3 网络基础TCP/IP
 - 通常使用的网络（包括互联网）是在TCP/IP协议族的基础上运作的。而HTTP属于它内部的一个子集。
 - 协议：协议是通信计算机双方必须共同遵从的一组约定（协议中存在各式各样的内容。从电缆的规格到IP地址的选定方法、寻找异地用户的方法、双方建立通信的顺序，以及Web页面显示需要处理的步骤）
 - TCP/IP：互联网相关协议的集合
![在这里插入图片描述](https://img-blog.csdnimg.cn/20210126090435504.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0FuaXRhU3Vu,size_16,color_FFFFFF,t_70)
#### 1.3.2 TCP/IP的分层管理
 - TCP/IP协议族按层次分别分为以下4层：应用层、传输层、网络层和数据链路层
 - 层次化的优点：
	便于修改：如果互联网只由一个协议统筹，某个地方需要改变设计时，就必须把所有部分整体替换掉。而分层之后只需把变动的层替换掉即可。把各层之间的接口部分规划好之后，每个层次内部的设计就能够自由改动了。
	设计简单：处于应用层上的应用可以只考虑分派给自己的任务，而不需要弄清对方在地球上哪个地方、对方的传输路线是怎样的、是否能确保传输送达等问题。
 - 各层的作用：
	应用层：
	![在这里插入图片描述](https://img-blog.csdnimg.cn/20210126091335976.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0FuaXRhU3Vu,size_16,color_FFFFFF,t_70)
	***
	传输层
	![在这里插入图片描述](https://img-blog.csdnimg.cn/20210126091620794.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0FuaXRhU3Vu,size_16,color_FFFFFF,t_70)
	***
	网络层（又名网络互连层）
	![在这里插入图片描述](https://img-blog.csdnimg.cn/20210126091859493.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0FuaXRhU3Vu,size_16,color_FFFFFF,t_70)
	***
	链路层（又名数据链路层，网络接口层）
	![在这里插入图片描述](https://img-blog.csdnimg.cn/20210126092041581.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0FuaXRhU3Vu,size_16,color_FFFFFF,t_70)
#### TCP/IP 通信传输流
![在这里插入图片描述](https://img-blog.csdnimg.cn/20210126092553124.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0FuaXRhU3Vu,size_16,color_FFFFFF,t_70)
 - 发送端从应用层往下走，接收端则往应用层往上走。
 - 作为发送端的客户端在应用层（HTTP协议）发出一个想看某个Web页面的HTTP请求
 - 为了传输方便，在传输层（TCP协议）把从应用层处收到的数据（HTTP请求报文）进行分割，并在各个报文上打上标记序号及端口号后转发给网络层。
 - 在网络层（IP协议），增加作为通信目的地的MAC地址后转发给链路层。这样一来，发往网络的通信请求就准备齐全了。
 - 接收端的服务器在链路层接收到数据，按序往上层发送，一直到应用层。当传输到应用层，才能算真正接收到由客户端发送过来的HTTP请求。
![在这里插入图片描述](https://img-blog.csdnimg.cn/20210126093347173.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0FuaXRhU3Vu,size_16,color_FFFFFF,t_70)
***
## 1.4 与HTTP关系密切的协议：IP、TCP和DNS
#### 1.4.1 负责传输的IP协议
 - IP（Internet Protocol）网际协议位于网络层
    IP其实是一种协议的名称
 - IP协议的作用是把各种数据包传送给对方
	IP地址指明了节点被分配到的地址，MAC地址是指网卡所属的固定地址。IP地址可以和MAC地址进行配对。IP地址可变换，但MAC地址基本上不会更改。
###### 使用ARP协议凭借MAC地址进行通信
 - IP间的通信依赖MAC地址。在连接到对方的时候，通常要经过多台计算机和网络设备中转。在进行中转时，会利用下一站中转设备的MAC地址来搜索下一个中转目标。
 - ARP是一种用以解析地址的协议，根据通信方的IP地址就可以反查出对应的MAC地址。

###### 没有人能够全面掌握互联网中的传输状况
 - 路由选择：
	在到达通信目标前的中转过程中，那些计算机和路由器等网络设备只能获悉很粗略的传输路线。
	![在这里插入图片描述](https://img-blog.csdnimg.cn/20210126095545121.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0FuaXRhU3Vu,size_16,color_FFFFFF,t_70)
#### 1.4.2 确保可靠性的TCP协议
 - TCP位于传输层，提供可靠的字节流服务
 - 字节流服务：为了方便传输，将大块数据分割成以报文段（segment）为单位的数据包进行管理
 - 可靠的传输服务：能够把数据准确可靠地传给对方
 - TCP协议为了更容易传送大数据才把数据分割，而且TCP协议能够确认数据最终是否送达到对方。
###### 确保数据能够到达目标
三次握手
 - 用TCP协议把数据包送出去后，TCP不会对传送后的情况置之不理，它一定会向对方确认是否成功送达。
 - 握手过程中使用了TCP的标志（flag）——SYN（synchronize）和ACK（acknowledgement）。
 - 发送端首先发送一个带SYN标志的数据包给对方。接收端收到后，回传一个带有SYN/ACK标志的数据包以示传达确认信息。最后，发送端再回传一个带ACK标志的数据包，代表“握手”结束。
 - 若在握手过程中某个阶段莫名中断，TCP协议会再次以相同的顺序发送相同的数据包。
![在这里插入图片描述](https://img-blog.csdnimg.cn/20210126100519364.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0FuaXRhU3Vu,size_16,color_FFFFFF,t_70)
***
## 1.5 负责域名解析的DNS服务
 - DNS（Domain Name System）服务是和HTTP协议一样位于应用层的协议。它提供域名到IP地址之间的解析服务。
![在这里插入图片描述](https://img-blog.csdnimg.cn/20210126101101883.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0FuaXRhU3Vu,size_16,color_FFFFFF,t_70)
***
## 1.6 各种协议与HTTP协议的关系
![在这里插入图片描述](https://img-blog.csdnimg.cn/20210126101343878.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0FuaXRhU3Vu,size_16,color_FFFFFF,t_70)
***
## 1.7 URI和URL
#### 1.7.1 统一资源标识符
URI（Uniform Resource Identifier）
 - Uniform：规定统一的格式可方便处理多种不同类型的资源，而不用根据上下文环境来识别资源指定的访问方式
 - Resource：资源的定义是“可标识的任何东西”。不仅是文档文件，图像或服务（例如当天的天气预报）等能够区别于其他类型的，全都可作为资源。另外，资源不仅可以是单一的，也可以是多数的集合体。
 - Identifier：表示可标识的对象。也称为标识符。

URI就是由某个协议方案表示的资源的定位标识符。协议方案是指访问资源所使用的协议类型名称。

URI用字符串标识某一互联网资源，而URL表示资源的地点（互联网上所处的位置）。可见URL是URI的子集。

 - 几种URI的例子
	![在这里插入图片描述](https://img-blog.csdnimg.cn/20210126102449260.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0FuaXRhU3Vu,size_16,color_FFFFFF,t_70)
#### 1.7.2 URI格式
 - 要表示指定的URI
	绝对URI：涵盖全部必要信息
	绝对URL：![在这里插入图片描述](https://img-blog.csdnimg.cn/20210126102916599.png)
	相对URL：是指从浏览器中基本URI处指定的URL，形如 /image/logo.gif。
![在这里插入图片描述](https://img-blog.csdnimg.cn/20210126103150850.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0FuaXRhU3Vu,size_16,color_FFFFFF,t_70)
![在这里插入图片描述](https://img-blog.csdnimg.cn/20210126103209791.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0FuaXRhU3Vu,size_16,color_FFFFFF,t_70)

## 3.1 HTTP报文
 - 分为请求报文和响应报文
	![在这里插入图片描述](https://img-blog.csdnimg.cn/20210127115238458.png)
## 请求报文和响应报文的结构
![在这里插入图片描述](https://img-blog.csdnimg.cn/20210127115538612.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0FuaXRhU3Vu,size_16,color_FFFFFF,t_70)
![在这里插入图片描述](https://img-blog.csdnimg.cn/20210127115627602.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0FuaXRhU3Vu,size_16,color_FFFFFF,t_70)
 - 请求行：包含用于请求的方法，请求URI和HTTP版本。
 - 状态行：包含表明响应结果的状态码，原因短语和HTTP版本。
 - 首部字段：包含表示请求和响应的各种条件和属性的各类首部。一般有4种首部，分别是：通用首部、请求首部、响应首部和实体首部。
 - 其他：可能包含HTTP的RFC里未定义的首部（Cookie等）。

***
## 3.3 编码提升传输速率
#### 3.3.1 报文主体和实体主体的差异
 - HTTP报文的`主体`用于传输请求或响应的`实体主体`。
 - 通常，*报文主体等于实体主体*。只有当传输中进行**编码**操作时，实体主体的内容发生变化，才导致它和报文主体产生差异。
#### 3.3.2 压缩传输的内容编码
常用的内容编码有以下几种。
 - gzip（GNU zip）
 - compress（UNIX系统的标准压缩）
 - deflate（zlib）
 - identity（不进行编码）
#### 3.3.3 分割发送的分块传输编码
 - 当传输大容量数据时，通过把数据分割成多块，能够让浏览器逐步显示页面
 - 分块传输编码会将实体主体分成多个部分（块）。每一块都会用十六进制来标记块的大小，而实体主体的最后一块会使用“0(CR+LF)”来标记。
![在这里插入图片描述](https://img-blog.csdnimg.cn/20210127155709661.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0FuaXRhU3Vu,size_16,color_FFFFFF,t_70)
***
## 3.4 发送多种数据的多部分对象集合
 - MIME：允许邮件处理文本、图片、视频等多个不同类型的数据。 在MIME扩展中会使用一种称为多部分对象集合（Multipart）的方法，来容纳多份不同类型的数据。
 - HTTP协议中也采纳了多部分对象集合：
	multipart/form-data：在Web表单文件上传时使用。
![在这里插入图片描述](https://img-blog.csdnimg.cn/20210127160728800.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0FuaXRhU3Vu,size_16,color_FFFFFF,t_70)
	multipart/byteranges：状态码206（Partial Content，部分内容）响应报文包含了多个范围的内容时使用。
	![在这里插入图片描述](https://img-blog.csdnimg.cn/20210127160811686.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0FuaXRhU3Vu,size_16,color_FFFFFF,t_70)

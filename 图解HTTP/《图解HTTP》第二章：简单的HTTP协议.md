## 2.1 HTTPЭ�����ڿͻ��˺ͷ�����֮���ͨ��
  - ��������ı���ͼ�����Դ��һ�˳�Ϊ`�ͻ���`�����ṩ��Դ��Ӧ��һ�˳�Ϊ`��������`��
  - ����̨�����֮��ʹ��HTTPЭ��ͨ��ʱ����һ��ͨ����·�ϱض���һ���ǿͻ��ˣ���һ�����Ƿ������ˡ�
  - ��̨�������Ϊ�ͻ��˺ͷ������˵Ľ�ɫ�п��ܻụ�������ͽ���һ��ͨ��·����˵���������˺Ϳͻ��˵Ľ�ɫ��ȷ���ģ�����HTTPЭ���ܹ���ȷ�����Ķ��ǿͻ��ˣ��Ķ��Ƿ������ˡ�


## 2.2 ͨ���������Ӧ�������ͨ��
 - �϶����ȴӿͻ��˿�ʼ����ͨ�ŵģ�����������û�н��յ�����֮ǰ���ᷢ����Ӧ��
![���������ͼƬ����](httpsimg-blog.csdnimg.cn20210126112017423.pngx-oss-process=imagewatermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0FuaXRhU3Vu,size_16,color_FFFFFF,t_70)
![���������ͼƬ����](httpsimg-blog.csdnimg.cn20210126112132531.png)
 - GET����ʾ������ʷ�����������
 - index.html��ָ����������ʵ���Դ��������URI��
 - HTTP1.1��HTTP�İ汾�ţ�������ʾ�ͻ���ʹ�õ�HTTPЭ�鹦�ܡ�

�������������󷽷�������URI��Э��汾����ѡ�������ײ��ֶκ�����ʵ�幹�ɵġ�
![���������ͼƬ����](httpsimg-blog.csdnimg.cn20210126112416111.pngx-oss-process=imagewatermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0FuaXRhU3Vu,size_16,color_FFFFFF,t_70)
������������
![���������ͼƬ����](httpsimg-blog.csdnimg.cn20210126112534655.pngx-oss-process=imagewatermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0FuaXRhU3Vu,size_16,color_FFFFFF,t_70)
 - HTTP1.1����ʾ��������Ӧ��HTTP�汾
 - 200 OK����ʾ����Ĵ�������״̬�루statuscode����ԭ����reason-phrase��
 - Data��������Ӧ������ʱ��

![���������ͼƬ����](httpsimg-blog.csdnimg.cn20210126112821294.pngx-oss-process=imagewatermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0FuaXRhU3Vu,size_16,color_FFFFFF,t_70)

## 2.3 HTTP�ǲ�����״̬��Э��
 - ��HTTP�������Э����ڷ��͹����������Ӧ�������־û�����
![���������ͼƬ����](httpsimg-blog.csdnimg.cn20210126113008287.pngx-oss-process=imagewatermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0FuaXRhU3Vu,size_16,color_FFFFFF,t_70)
 - ʹ��HTTPЭ�飬ÿ�����µ�������ʱ���ͻ��ж�Ӧ������Ӧ������
 - HTTP1.1��Ȼ����״̬Э�飬��Ϊ��ʵ�������ı���״̬���ܣ�����������Cookie����

## 2.4 ����URI��λ��Դ
 - HTTPЭ��ʹ��URI��λ�������ϵ���Դ
 - ָ������URI�ķ�ʽ��
	![���������ͼƬ����](httpsimg-blog.csdnimg.cn20210126113353706.pngx-oss-process=imagewatermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0FuaXRhU3Vu,size_16,color_FFFFFF,t_70)
 - ������Ƿ����ض���Դ���ǶԷ��������������󣬿�����һ������������URI��������������ǲ�ѯHTTP��������֧�ֵ�HTTP�������ࡣ
	![���������ͼƬ����](httpsimg-blog.csdnimg.cn20210126113500343.png)

## 2.5 ��֪��������ͼ��HTTP����
HTTP1.1 �п�ʹ�õķ�����

#### GET����ȡ��Դ
 - GET����������������ѱ�URIʶ�����Դ��ָ������Դ���������˽����󷵻���Ӧ����
 - ����������Դ���ı����Ǿͱ���ԭ�����أ��������CGI��Common GatewayInterface��ͨ�����ؽӿڣ������ĳ����򷵻ؾ���ִ�к����������
![���������ͼƬ����](httpsimg-blog.csdnimg.cn20210126113938945.pngx-oss-process=imagewatermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0FuaXRhU3Vu,size_16,color_FFFFFF,t_70)
#### POST������ʵ������
 - ��Ȼ��GET����Ҳ���Դ���ʵ������壬��һ�㲻��GET�������д��䣬������POST����
![���������ͼƬ����](httpsimg-blog.csdnimg.cn20210126114548361.png)
#### PUT�������ļ�
 - Ҫ���������ĵ������а����ļ����ݣ�Ȼ�󱣴浽����URIָ����λ�á�
 - ����HTTP1.1��PUT������������֤���ƣ��κ��˶������ϴ��ļ������ڰ�ȫ�����⣬���һ���Web��վ��ʹ�ø÷���
![���������ͼƬ����](httpsimg-blog.csdnimg.cn20210126115148147.pngx-oss-process=imagewatermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0FuaXRhU3Vu,size_16,color_FFFFFF,t_70)
#### HEAD����ñ����ײ�
 - HEAD������GET����һ����ֻ�ǲ����ر������岿�֡�����ȷ��URI����Ч�Լ���Դ���µ�����ʱ��ȡ�
![���������ͼƬ����](httpsimg-blog.csdnimg.cn20210126115622954.png)
#### DELETE��ɾ���ļ�
 - HTTP1.1��DELETE���������PUT����һ��������֤���ƣ�����һ���Web��վҲ��ʹ��DELETE�����������WebӦ�ó������֤���ƣ�������REST��׼ʱ�����п��ܻῪ��ʹ�õġ�
![���������ͼƬ����](httpsimg-blog.csdnimg.cn20210126115807349.png)
#### OPTIONS��ѯ��֧�ֵķ���
 - OPTIONS����������ѯ�������URIָ������Դ֧�ֵķ�����
![���������ͼƬ����](httpsimg-blog.csdnimg.cn20210126135745995.png)
#### TRACE��׷��·��
 - TRACE��������Web�������˽�֮ǰ������ͨ�Ż��ظ��ͻ��˵ķ�����
 - ��������ʱ����Max-Forwards�ײ��ֶ���������ֵ��ÿ����һ���������˾ͽ������ּ�1������ֵ�պü���0ʱ����ֹͣ�������䣬�����յ�����ķ��������򷵻�״̬��200 OK����Ӧ��
 - TRACE���������Ͳ���ô���ã��ټ�������������XST��Cross-Site Tracing����վ׷�٣�������ͨ���͸������õ��ˡ�
![���������ͼƬ����](httpsimg-blog.csdnimg.cn20210126140242475.png)
## CONNECT��Ҫ�������Э�����Ӵ���
 - CONNECT����Ҫ��������������ͨ��ʱ���������ʵ�������Э�����TCPͨ�š���Ҫʹ��SSL��Secure SocketsLayer����ȫ�׽Ӳ㣩��TLS��Transport Layer Security������㰲ȫ��Э���ͨ�����ݼ��ܺ�����������䡣
![���������ͼƬ����](httpsimg-blog.csdnimg.cn20210126140341338.png)

## 2.6 ʹ�÷����´�����
 - ����������ָ���������Դ����������ĳ����Ϊ����������GET��POST��HEAD�ȡ�
![���������ͼƬ����](httpsimg-blog.csdnimg.cn20210126140756117.pngx-oss-process=imagewatermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0FuaXRhU3Vu,size_16,color_FFFFFF,t_70)

## 2.7 �־����ӽ�ʡͨ����
 - HTTPЭ��ĳ�ʼ�汾�У�ÿ����һ��HTTPͨ�ž�Ҫ�Ͽ�һ��TCP���ӡ�
![���������ͼƬ����](httpsimg-blog.csdnimg.cn20210126141028873.pngx-oss-process=imagewatermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0FuaXRhU3Vu,size_16,color_FFFFFF,t_70)
�������һ�ݰ�������ͼƬ��HTML�ĵ��������������ͨ�ſ���

#### 2.7.1 �־�����
 - ֻҪ����һ��û����ȷ����Ͽ����ӣ��򱣳�TCP����״̬����HTTP1.1��һ���ֵ�HTTP1.0��
	![���������ͼƬ����](httpsimg-blog.csdnimg.cn20210126141546325.pngx-oss-process=imagewatermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0FuaXRhU3Vu,size_16,color_FFFFFF,t_70)
#### 2.7.2 ���߻�
 - ���߻��������ֺ󣬲��õȴ���Ӧ���ֱ�ӷ�����һ������
 ![���������ͼƬ����](httpsimg-blog.csdnimg.cn20210126141959481.pngx-oss-process=imagewatermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0FuaXRhU3Vu,size_16,color_FFFFFF,t_70)

## 2.8 ʹ��Cookie��״̬����
 - HTTP����״̬Э�飬������֮ǰ���������������Ӧ��״̬���й���
 - Cookie����ͨ�����������Ӧ������д��Cookie��Ϣ�����ƿͻ��˵�״̬��
![���������ͼƬ����](httpsimg-blog.csdnimg.cn2021012614254550.pngx-oss-process=imagewatermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0FuaXRhU3Vu,size_16,color_FFFFFF,t_70)
![���������ͼƬ����](httpsimg-blog.csdnimg.cn20210126142652500.pngx-oss-![���������ͼƬ����](httpsimg-blog.csdnimg.cn20210126142709362.pngx-oss-process=imagewatermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0FuaXRhU3Vu,size_16,color_FFFFFF,t_70)
![���������ͼƬ����](httpsimg-blog.csdnimg.cn20210126142725264.pngx-oss-process=imagewatermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0FuaXRhU3Vu,size_16,color_FFFFFF,t_70)

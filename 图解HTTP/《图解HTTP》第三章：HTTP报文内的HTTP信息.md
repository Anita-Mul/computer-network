## 3.1 HTTP����
 - ��Ϊ�����ĺ���Ӧ����
	![���������ͼƬ����](https://img-blog.csdnimg.cn/20210127115238458.png)
## �����ĺ���Ӧ���ĵĽṹ
![���������ͼƬ����](https://img-blog.csdnimg.cn/20210127115538612.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0FuaXRhU3Vu,size_16,color_FFFFFF,t_70)
![���������ͼƬ����](https://img-blog.csdnimg.cn/20210127115627602.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0FuaXRhU3Vu,size_16,color_FFFFFF,t_70)
 - �����У�������������ķ���������URI��HTTP�汾��
 - ״̬�У�����������Ӧ�����״̬�룬ԭ������HTTP�汾��
 - �ײ��ֶΣ�������ʾ�������Ӧ�ĸ������������Եĸ����ײ���һ����4���ײ����ֱ��ǣ�ͨ���ײ��������ײ�����Ӧ�ײ���ʵ���ײ���
 - ���������ܰ���HTTP��RFC��δ������ײ���Cookie�ȣ���

***
## 3.3 ����������������
#### 3.3.1 ���������ʵ������Ĳ���
 - HTTP���ĵ�`����`���ڴ����������Ӧ��`ʵ������`��
 - ͨ����*�����������ʵ������*��ֻ�е������н���**����**����ʱ��ʵ����������ݷ����仯���ŵ������ͱ�������������졣
#### 3.3.2 ѹ����������ݱ���
���õ����ݱ��������¼��֡�
 - gzip��GNU zip��
 - compress��UNIXϵͳ�ı�׼ѹ����
 - deflate��zlib��
 - identity�������б��룩
#### 3.3.3 �ָ�͵ķֿ鴫�����
 - ���������������ʱ��ͨ�������ݷָ�ɶ�飬�ܹ������������ʾҳ��
 - �ֿ鴫�����Ὣʵ������ֳɶ�����֣��飩��ÿһ�鶼����ʮ����������ǿ�Ĵ�С����ʵ����������һ���ʹ�á�0(CR+LF)������ǡ�
![���������ͼƬ����](https://img-blog.csdnimg.cn/20210127155709661.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0FuaXRhU3Vu,size_16,color_FFFFFF,t_70)
***
## 3.4 ���Ͷ������ݵĶಿ�ֶ��󼯺�
 - MIME�������ʼ������ı���ͼƬ����Ƶ�ȶ����ͬ���͵����ݡ� ��MIME��չ�л�ʹ��һ�ֳ�Ϊ�ಿ�ֶ��󼯺ϣ�Multipart���ķ����������ɶ�ݲ�ͬ���͵����ݡ�
 - HTTPЭ����Ҳ�����˶ಿ�ֶ��󼯺ϣ�
	multipart/form-data����Web���ļ��ϴ�ʱʹ�á�
![���������ͼƬ����](https://img-blog.csdnimg.cn/20210127160728800.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0FuaXRhU3Vu,size_16,color_FFFFFF,t_70)
	multipart/byteranges��״̬��206��Partial Content���������ݣ���Ӧ���İ����˶����Χ������ʱʹ�á�
	![���������ͼƬ����](https://img-blog.csdnimg.cn/20210127160811686.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L0FuaXRhU3Vu,size_16,color_FFFFFF,t_70)

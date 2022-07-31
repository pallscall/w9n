---
title: wireshark录制grpc
tags: article
---

> 本地构造grpc client端与server端，跳过～


## 一、创建proto文件目录以及第三方包文件目录
比如程序用到了 hello.proto 文件，那么就将 hello.proto 单独放在一个目录中，第三方包（诸如 google、github 等）同理。

**切记！！！** 不要将 应用proto文件与第三方proto文件放在同一个目录中，会有概率导致后续grpc格式解析失败。

## 二、抓包
![在这里插入图片描述](https://img-blog.csdnimg.cn/ab91142abb254f7ea9f4429d9d33e50c.png)
## 三、协议转换
![在这里插入图片描述](https://img-blog.csdnimg.cn/34ffab246ac04b9a8951b97880d58dcc.png)
![在这里插入图片描述](https://img-blog.csdnimg.cn/ca5f2bf3e85f40fcb0dcc2751e67f730.png)
## 四、配置proto文件搜索路径
Wireshark ---- Preference ---- Protocols ---- Protobuf

![在这里插入图片描述](https://img-blog.csdnimg.cn/12a9ed243690478380028a345177b739.png)

![在这里插入图片描述](https://img-blog.csdnimg.cn/af267fc54f0d4fd9a10b656ebc330c26.png)

然后ok ok ok

然后

![在这里插入图片描述](https://img-blog.csdnimg.cn/8843a096cc6c46bd9b8530656f5a7b93.png)
大功告成
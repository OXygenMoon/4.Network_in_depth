<p align='center'>
<a href="https://oxygenpanda.github.io/" target="_blank"><img alt="Website" src="https://img.shields.io/badge/博客-劳振煜的知識倉儲-faf2f2.svg?style=flat-square&logo=Blogger"></a>
<a href="https://www.github.com/OXygenPanda" target="_blank"><img src="https://img.shields.io/badge/Github-@劳振煜-f3e1e1.svg?style=flat-square&logo=GitHub"></a>
<a href="https://i.loli.net/2020/11/11/SBZ2mFJGKLjUtTO.jpg" target="_blank"><img src="https://img.shields.io/badge/微信-@OXygen-f1d1d1.svg?style=flat-square&logo=WeChat"></a>


# 计算机网络 第六章

>   第六章的主要内容是 : 应用层

## 域名系统 DNS

**负责解析域名**

DNS服务器解析我们输入的域名成对应的IP地址.

根 .

顶级域名 com edu net cn org gov

二级域名 oxygenn

三级域名 dba

**域名解析测试**

>   ping [www.baidu.com](http://www.baidu.com)

>   nslookup

**域名服务器**

每一个类型的DNS服务器都会有多台, 负载均衡

根DNS 只知道顶级域名该去找谁

COM 101

NET 102

EDU 103

CN 104

**安装自己的DNS服务器**

1.  解析内网自己的域名
2.  私网内可以设置一个DNS服务器, 用于缓存外网解析得到的IP地址

## 动态主机配置协议 DHCP

静态IP地址 : 主机位置固定的话, 使用静态IP地址较为方便

动态IP地址 : 主机位置移动, 使用动态IP地址较为方便

DHCP从IP池中动态分配IP地址

## 文件传送协议 FTP

数据连接的建立类型 :

-   主动模式 : FTP客户端告诉服务器使用的端口侦听,  FTP服务器的20端口向客户端发起连接
    -   主动模式需要在服务器防火墙上打开20和21端口(安全性)
-   被动模式 : FTP服务器告诉客户端使用的端口侦听, FTP客户端的某一端口发起连接
    -   被动模式需要服务器防火墙打开大量端口

控制连接 : 标准端口是21, 发送FTP命令信息

数据连接 : 标准端口是20, 上传,下载数据

FTP传输模式 :

-   文本模式 : ASCII模式, 以文本序列传输数据
-   二进制模式 : Binary模式, 以二进制序列传输数据

## 远程终端协议 TELNET

默认端口号 : TCP 23

远程控制路由器, windows主机

## 电子邮件 SMTP POP3 IMAP

SMTP 发送

POP3 IMAP 接收

## 超文本传输协议 HTTP

**统一资源定位符URL**

<协议>://<主机>:<端口>/<路径>

网站的标识可以用不同端口或者不同的IP地址或者不同的域名来区别

**使用Web代理服务器访问网站**

1.  节省内网访问Internet的带宽(代理服务器缓存一些静态资源)
2.  通过Web代理访问绕过防火墙
3.  避免IP地址跟踪
4.  可能会加速可能会减速

**请求方法类型**

OPTIONS : 请求一些选项信息, 允许客户端查看服务器的性能

GET : 请求指定的页面信息, 并返回实体主体

HEAD : 类似于get请求, 只不过返回的响应中没有具体内容, 用于获取报头

POST : 向指定资源提交数据进行处理请求(例如提交表单或者上传文件). 会导致文件修改.

PUT : 从客户端向服务器传送的数据取代指定的文档的内容

DELETE : 请求服务器删除指定的页面

TRACE : 回显服务器收到的请求, 主要用于测试或诊断

**状态码**

1xx : 表示通知信息, 如请求收到了或正在进行处理

-   100 Continue : 继续, 客户端继续其请求
-   101 Switching Protocols 切换协议, 服务器根据客户端的请求切换协议

2xx : 表示成功, 如接收或知道了

-   200  OK : 请求成功

3xx : 表示重定向, 如要完成请求必须采取进一步的行动

-   301 Moved Permanently : 永久移动.

4xx : 表示客户的差错, 如请求中有错误的语法或不能完成

-   400 Bad Request : 客户端请求的语法错误, 服务器无法理解
-   401 Unauthorized : 请求要求用的身份认证
-   403 Forbidden : 服务器拒绝执行客户端请求
-   404 Not Found : 服务器无法根据客户端的请求找到资源.
-   408 Request Timeout : 请求超时

5xx : 表示服务器的差错, 如服务器失效无法完成请求

-   500 Internal Server Error : 服务器内部错误, 无法完成请求
-   503 Service Unavailable : 超载或系统维护
-   504 Gateway Timeout : 充当网关或代理的服务器, 获取资源超时

## HTTPs

补充学习 :

[HTTP | CS-Notes](http://www.cyc2018.xyz/计算机基础/HTTP/HTTP.html#一-、基础概念)
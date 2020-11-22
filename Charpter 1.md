<p align='center'>
<a href="https://oxygenpanda.github.io/" target="_blank"><img alt="Website" src="https://img.shields.io/badge/博客-劳振煜的知識倉儲-faf2f2.svg?style=flat-square&logo=Blogger"></a>
<a href="https://www.github.com/OXygenPanda" target="_blank"><img src="https://img.shields.io/badge/Github-@劳振煜-f3e1e1.svg?style=flat-square&logo=GitHub"></a>
<a href="https://i.loli.net/2020/11/11/SBZ2mFJGKLjUtTO.jpg" target="_blank"><img src="https://img.shields.io/badge/微信-@OXygen-f1d1d1.svg?style=flat-square&logo=WeChat"></a>
# # 计算机网络 第一章

>   计算机网络第一章的主要内容是 : 概述

## 课程安排

第一章 : 概述

第二章 : 物理层

第三章 : 数据链路层

第四章 : 网络层

第五章 : 运输层

第六章 : 应用层

第七章 : 网络安全

第八章 : 因特网上的音频,视频服务

第九章 : 无线网络

第十章 : 下一代因特网

## 计算机网络在信息时代的作用

21世纪的特征 : 数字化, 网络化, 信息化

网络化 : 三网(电信网络, 计算机网络, 有线电视网络)

计算机网络 : 因特网, 其他网络(政府网络, 军用网络)

### 计算机网络的重要功能

连通性 : 彼此联通, 交换信息

共享 : 信息共享, 软硬件共享(软 : ssh ; 硬 : 打印机等设备)

## 因特网概述

终端到网络(路由器)的距离大约是100米, 路由器与路由器的连接扩展了网络的距离和接入网设备的数量.

### 概念

网络 : 许多计算机连接在一起

互联网 : 许多网络连接在一起 (internet)

因特网 : 全球最大的一个互联网 (Internet, 使用 TCP/IP 协议)

### 因特网发展的三个阶段

1st : ARPANET向互联网发展 (上世纪60年代 - 80 年代中期)

-   1969年 分组交换网
-   1975年 互联网
-   1983年 TCP/IP (因特网起源)

2nd : 三级结构的因特网 (上世纪80年代中期 - 90 年代初期)

-   分层次, 比如 : 学校网 - 区域网 - 主干网(带宽 : 45 M)

3rd : 多层次ISP结构的因特网

-   ISP : Internet Service Provider 因特网服务提供商
-   第一层ISP - 第二层ISP - 第三层ISP(提供接入) - 校园网等
-   如果服务器需要提供的客户范围较小, 应该接入越低层的ISP

### 因特网的标准化工作

因特网协会 : ISOC

因特网体系结构委员会 IAB :

-   因特网研究部 IRTF :
    -   因特网研究指导小组 IRSG
-   因特网工程部 IETF :
    -   因特网工程指导小组 IESG

### 因特网的组成

**因特网的核心部分**

**因特网的边缘部分**

主机之间的通信方式 :

-   客户端服务器方式 (Client / Server 方式)
-   对等方式 (Peer-to-Peer 方式)

数据交换方式 :

-   电路交换 (Circuit Switching)
    -   交换机同时只能提供网络中的两个终端通信
    -   过程 : 申请占用通信资源, 一直占用通信资源, 释放通信资源
    -   适用于 : 实时性通信, 核心路由器之间可以使用电路交换
-   报文交换 (Message Switching)
    -   报文一般比分组长的多
    -   报文交换的时延较长
-   分组交换 (Packet Switching)
    -   完整的一个数据包称为报文, 需要分为多个组进行发送
    -   每一个分组带上一个首部
    -   分组的优势在于, 通信时路径可以复用
    -   接收端去电首部后, 拼接分组成报文
    -   路由器有存储转发功能
    -   优点 : 高效, 灵活, 迅速, 可靠
    -   问题 : 时延, 开销
NekoIM
======

「猫聊 ~ NekoIM」——为不同平台的宅们提供多元聊天的一次尝试

* Homepage(主页) : http://im.nekonazo.com/
* Wiki(文档) : http://wiki.oekaki.so/NekoIM
* BBS(讨论) : http://bbs.nekonazo.com/u80.1/
* Blog(更新履历) : http://oekaki.so/?c=nekoim
* 发布者 : 同人企画 Project Oekakisoli ( http://oekaki.so )
目前正处在Alpha测试阶段。

所要达到的
-------------
* 普通用户：
  * 通过XMPP Gateway，不同社区或传输协议的人使用原有ID实现基于PC/MAC/移动设备的即时聊天/多人聊天成为可能
* 开发者：
  * 可利用猫聊开放平台接入，测试新的自制应用，之后可以推广到与平台挂接的更多社区。
  * 或将猫聊开放平台中的一项或多项应用接入自己维护的SNS，聊天室，游戏大厅或任意需要用户交流的社区，可DIY跨传输协议的接口
  * 亦可利用猫聊开放平台向需要的社区统一推送或订阅消息，实现向自己的用户广播和通知功能

具体实现
-------------
* 服务端 - 在过去的半年里横向测试了ejabberd,Openfire和Tigase。而最终Tigase的overhead最小和稳定性最高，以及没有前两者的跨服务器传输大量数据频繁断开和出错的问题。于是基于Tigase做了一个fork，主要追加对i18N和本土化支持，修复数个SASL的UTF-8解析错误，将来还会做一些优化和增加插件例如用户搜索。最终采用Tigase (Cluster) + Postgresql （说起来最近研究Tigase的人貌似突然变多了
* 客户端
  * Windows - 基于Miranda NG的Custom Pack。猫聊主要完成了一个比官方完整很多的中文翻译包和自制界面，集成了Nekonazo娘的表情，并且通过长时间的聊天习惯总结优化和简化了大量默认配置，对字体方案优化。
  * MAC
  * Linux
  * Android - Xabber+中文完整翻译+默认配置本土化+内置表情识别
  * iOS - 由于未找到专门支持XMPP的开源客户端所以还在筹备阶段。但已经有相当多的兼容XMPP的客户端。随后会发一份到wiki
* 开放平台
  * 萌娘回路
  * 更新姬
  * MoeID (?)
  * etc

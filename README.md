本文的基本介绍
***
# 国内网络基本了解
大家都知道，我们中国对网络的限制比较严格，不是所有的网站咱们都能浏览。国家主要通过GFW([dns劫持](https://baike.baidu.com/item/%E5%9F%9F%E5%90%8D%E5%8A%AB%E6%8C%81/7657893?fromtitle=DNS%E5%8A%AB%E6%8C%81&fromid=6739044&fr=aladdin)、[dns污染](https://baike.baidu.com/item/DNS%E6%B1%A1%E6%9F%93)和[ip封锁](https://baike.baidu.com/item/ip%E5%B0%81%E9%94%81)等手段)进行网络封锁。下图是百度百科对GFW（俗称“墙”）的介绍（点击图片可查看详细介绍）
[![GFW](https://www.louimg.com/u/20200312/11050110.png "点击图片查看GFW的介绍")]
大家主要看红圈里的文字，GFW的功劳：让国民政治觉悟提升了不少，所以GFW只会越来越完善。但对于大多数网民来说，网络是我们学习、工作、美好生活的重要工具，GFW一定程度上把好多对我们学习、工作有帮助的综合性很强的技术、学术网站、社交网站等也拒之门外。
<br>大家经常听说的网站如[油管YouTube](https://www.youtube.com)、[脸书Facebook](https://www.facebook.com/)、[推特Twitter](https://twitter.com)、[电报telegram](https://telegram.org/)、[谷歌google](https://www.google.com.hk/)、[维基百科](https://zh.wikipedia.org/)等，这些我们都是无法正常访问的。需要科学上网（俗称翻墙）才能上。所以，这种背景下，也就出现了各种各样的突破GFW限制的工具，突破网络审查的软件通常被称作翻墙软件，俗称梯子。翻墙软件并不只是大家理解的VPN软件，还有基于其它协议的代理软件。
 ***
# 科学上网
## 没落的“VPN”
#### 1. 什么是VPN 
VPN全称“虚拟私人网络（Virtual Private Network）”，VPN是一个统称。VPN是一种加密通讯技术，它被设计出来的目的是数据传输安全和网络匿名。它有很多的具体实现，比如PPTP、L2TP、IPSec和openvpn。它的出现远早于GFW，所以它不是为了翻墙而生的，维基百科里关于VPN的介绍，说它的特殊使用才是翻墙。
[![VPN](https://www.louimg.com/u/20200312/15453995.png "点击图片查看VPN的维基介绍")]
GFW机制加上劳动人民的无穷智慧，促使聪慧的劳动人民开始用VPN连接外国网络实现翻墙，随着使用人数的激增和网络环境的发展，商业化的一键VPN也逐渐成熟，一些免费VPN和付费VPN就这样诞生了。
#### 2. VPN现状
使用 VPN，不足之处在于数据分流不灵活，会将开启了VPN的设备的所有数据流量全部导向至VPN服务器上；另外如果VPN服务器上有流量监视软件运行，那么用户所传输的数据将有信息安全威胁；进一步来说，由于VPN设计的初衷并不是用于翻墙，因此数据流量的特征非常明显，容易引起审查机构注意，导致被封。所以，VPN这种翻墙方式基本已经没落了。之前用过的蓝灯、赛风、自由门等这些熟悉的工具，现在已经很少有人用了，著名的老牌付费VPN供应商ExpressVPN还在坚挺中，但给本人的体验感极差，唯一一点好的就是能试用一个月，不满意全额退款。可能我买的时候正好是特殊时期吧（接近六四时购买），所以连不上也正常，只能这样安慰自己了。至于免费的VPN，由于用户人数与流量众多，常会暴露出了公共网络服务的特质，所以经常会被封。还有蓝鲸、老王VPN等，只能说你偶尔GHS的话，如果实在没有可用的，可以适当用一下。
#### 3. 先入为主的“翻墙”
VPN作为过去很长一段时间最主流最热门最常用最为人所知的翻墙手段，已然成为翻墙的代名词。即便是VPN已不再常用的今天，当人们谈及翻墙的时候，说得最多的仍是：“你有什么好用的vpn吗？”<br>
时代在进步，GFW也在不断加强，科学上网技术也要不断更新，更高效、安全性更高、速度更快的科学上网技术迟早会替代VPN成为新的霸主。
## 关于`[机场](https://stc-spades-beta1.com/auth/register?code=9JIx)`
### 1. 什么是`[机场](https://stc-spades-beta1.com/auth/register?code=9JIx)`
随着VPN的没落，现在主流的科学上网方式是大家经常听的SS（Shadowsocks）、ssr（ShadowsocksR）、V2(v2ray)、Trojan等等这些代理工具，还有基于这些代理工具的原理，扩展衍生出的在各平台使用且支持以上几种翻墙协议的科学上网工具，如clash、shadowrocket、Quantumult、Pharos Pro等等非常多。<br>
这些工具的统一特点就是：需要自行在服务端和客户端上部署，比一键VPN方法更“繁琐”，但优点就是更加安全、速度更快。其中服务端的部署有两种情况：一种是我们自己购买vps部署，这就是人们常说的我自己搭建节点。第二种，也是目前用的最多的方式，就是`[机场](https://stc-spades-beta1.com/auth/register?code=9JIx)`。
### 2. `[机场](https://stc-spades-beta1.com/auth/register?code=9JIx)`的选择



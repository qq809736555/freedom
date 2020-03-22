本文是一个微成熟小白对于科学上网的一些切身感受的整理，自己捋思路，同时也为方便他人。顺便会不断更新一些实用资源、工具等。发现错误的地方欢迎斧正。正文中点击“回到顶部”四个字即可回到目录，点击目录也会跳到相应模块。<br>`2020年3月16日更新：新增v2ray官方使用手册`
* [一、国内网络基本了解](#一国内网络基本了解)<br>
* [二、科学上网](#二科学上网)<br>
  * [No1、没落的“VPN”](#没落的VPN)<br>
    * [什么是VPN](#1-什么是VPN )<br>
    * [VPN现状](#2-VPN现状)<br>
    * [先入为主的“翻墙](#3-先入为主的翻墙)<br>
  * [No2、关于机场](#关于机场)<br>
    * [什么是机场](#1-什么是机场)<br>
    * [机场的选择](#2-机场的选择)<br>
      * [技术层面](#技术层面)<br>
        * [BGP中转和IPLC的通俗理解](#bgp中转和iplc的通俗理解)<br>
      * [主观层面](#主观层面)<br>
        * [机场的外观设计](#机场的外观设计)<br>
        * [机场电报群观察交流](#机场电报群观察交流)<br>
        * [机场的测速](#机场的测速)<br>
        * [机场价格](#机场价格)<br>
  * [No3、我的机场使用感受](#我的机场使用感受)<br>
* [三、主流科学上网工具下载(包含Win、Mac、Android三大平台)](#三主流科学上网工具下载包含winmacandroid三大平台)<br>
  * [Shadowsocks](#Shadowsocks简称SS)
  * [ShadowsocksR](#ShadowsocksR简称SSR)
  * [V2ray(含官方使用手册)](#V2ray简称V2)
  * [clash(含CFW使用说明书)](#clash)
    * [Clash.for.Windows汉化版，支持SSR和V2订阅](#ClashforWindows汉化版支持SSR和V2订阅)  
  * [Trojan](#Trojan)
  * [Mellow](#Mellow)<br>
  * [Netch(Win)](#netch)<br>
  * [Pharos Pro(Android)](#pharos-pro)<br>
* [四、其它实用资源、工具](#四其它实用资源工具)
***

# 一、国内网络基本了解
大家都知道，我们中国对网络的限制比较严格，不是所有的网站咱们都能浏览。国家主要通过GFW([dns劫持](https://baike.baidu.com/item/%E5%9F%9F%E5%90%8D%E5%8A%AB%E6%8C%81/7657893?fromtitle=DNS%E5%8A%AB%E6%8C%81&fromid=6739044&fr=aladdin)、[dns污染](https://baike.baidu.com/item/DNS%E6%B1%A1%E6%9F%93)和[ip封锁](https://baike.baidu.com/item/ip%E5%B0%81%E9%94%81)等手段)进行网络封锁。下图是百度百科对GFW（俗称“墙”）的介绍
[![GFW](https://www.louimg.com/u/20200312/11050110.png "GFW的介绍")]
大家主要看红圈里的文字，GFW的功劳：让国民政治觉悟提升了不少，所以GFW只会越来越完善。但对于大多数网民来说，网络是我们学习、工作、美好生活的重要工具，GFW一定程度上把好多对我们学习、工作有帮助的综合性很强的技术、学术网站、社交网站等也拒之门外。
<br>大家经常听说的网站如[油管YouTube](https://www.youtube.com)、[脸书Facebook](https://www.facebook.com/)、[推特Twitter](https://twitter.com)、[电报telegram](https://telegram.org/)、[谷歌google](https://www.google.com.hk/)、[维基百科](https://zh.wikipedia.org/)等，这些我们都是无法正常访问的。需要科学上网（俗称翻墙）才能上。所以，这种背景下，也就出现了各种各样的突破GFW限制的工具，突破网络审查的软件通常被称作翻墙软件，俗称梯子。翻墙软件并不只是大家理解的VPN软件，还有基于其它协议的代理软件。[回到顶部](#readme)
***

# 二、科学上网
## 没落的“VPN”
#### 1. 什么是VPN 
VPN全称“虚拟私人网络（Virtual Private Network）”，VPN是一个统称。VPN是一种加密通讯技术，它被设计出来的目的是数据传输安全和网络匿名。它有很多的具体实现，比如PPTP、L2TP、IPSec和openvpn。它的出现远早于GFW，所以它不是为了翻墙而生的，维基百科里关于VPN的介绍，说它的特殊使用才是翻墙。
[![VPN](https://www.louimg.com/u/20200312/15453995.png "VPN的维基介绍")]
GFW机制加上劳动人民的无穷智慧，促使聪慧的劳动人民开始用VPN连接外国网络实现翻墙，随着使用人数的激增和网络环境的发展，商业化的一键VPN也逐渐成熟，一些免费VPN和付费VPN就这样诞生了。[回到顶部](#readme)
#### 2. VPN现状
使用 VPN，不足之处在于数据分流不灵活，会将开启了VPN的设备的所有数据流量全部导向至VPN服务器上；另外如果VPN服务器上有流量监视软件运行，那么用户所传输的数据将有信息安全威胁；进一步来说，由于VPN设计的初衷并不是用于翻墙，因此数据流量的特征非常明显，容易引起审查机构注意，导致被封。所以，VPN这种翻墙方式基本已经没落了。之前用过的蓝灯、赛风、自由门等这些熟悉的工具，现在已经很少有人用了，著名的老牌付费VPN供应商ExpressVPN还在坚挺中，但给本人的体验感极差，唯一一点好的就是能试用一个月，不满意全额退款。可能我买的时候正好是特殊时期吧（接近六四时购买），所以连不上也正常，只能这样安慰自己了。至于免费的VPN，由于用户人数与流量众多，常会暴露出了公共网络服务的特质，所以经常会被封。还有蓝鲸、老王VPN等，只能说你偶尔GHS的话，如果实在没有可用的，可以适当用一下。[回到顶部](#readme)
#### 3. 先入为主的“翻墙”
VPN作为过去很长一段时间最主流最热门最常用最为人所知的翻墙手段，已然成为翻墙的代名词。即便是VPN已不再常用的今天，当人们谈及翻墙的时候，说得最多的仍是：“你有什么好用的vpn吗？”<br>
时代在进步，GFW也在不断加强，科学上网技术也要不断更新，更高效、安全性更高、速度更快的科学上网技术迟早会替代VPN成为新的霸主。[回到顶部](#readme)
***

## 关于[机场](https://stc-spades-beta1.com/auth/register?code=9JIx)
### 1. 什么是[机场](https://stc-spades-beta1.com/auth/register?code=9JIx)
随着VPN的没落，现在主流的科学上网方式是大家经常听的SS（Shadowsocks）、ssr（ShadowsocksR）、V2(v2ray)、Trojan等等这些代理工具，还有基于这些代理工具的原理，扩展衍生出的在各平台使用且支持以上几种翻墙协议的科学上网工具，如clash、shadowrocket、Quantumult、Pharos Pro等等非常多。<br>
这些工具的统一特点就是：工具自身没有翻墙功能，需要自行在服务端和客户端上部署，优点就是更加安全、速度更快，看似比一键VPN方法“繁琐”，但实际操作非常简单，其中服务端的部署有两种情况：<br>
第一种是我们自己购买vps部署，这就是人们常说的我自己搭建节点，喜欢折腾的伙伴可以自己去购买vps搭建，网上教程非常多<br>
第二种，就是有人替我们部署好了，直接用就可以。这也是目前用的最多的科学上网方式，提供这项服务的就是[机场](https://stc-spades-beta1.com/auth/register?code=9JIx)。<br>
服务端部署好后，我们只需将服务器地址、端口这些基本信息添加到我们电脑或手机上的代理工具里，这就是客户端部署，这就实现了科学上网。现在很多工具都支持一键订阅，多数机场也提供了订阅链接，不需要我们手动逐一添加节点。[回到顶部](#readme)
### 2. [机场](https://stc-spades-beta1.com/auth/register?code=9JIx)的选择
#### 技术层面
##### BGP中转和IPLC的通俗理解
大家在购买机场时候，会经常见到BGP中转、IPLC专线这些名词。至于他们的专业意义，自行google查询。对于很多不是专业研究这个的伙伴，就算我们查询了，也可能是似懂非懂的状态，所以这里不会给大家去深挖那些专业概念，我们尽量从小白角度出发，明白他们的所起的作用就行。<br>
首先，我们要了解的就是我们的电脑、手机通过机场翻墙，数据经历了一个什么过程，大致有以下几种类型（从专业角度讲，有些地方可能不是很恰当，但很形象）：
* 直连<br>
  * 用户 -> ss、ssr等协议 -> 公网传输穿过GFW -> 国外服务器<br>
大多数机场节点都是这种，尤其是一些免费节点。此方式成本低，因为是协议直接过GFW，虽然协议本身也做了技术处理，但大流量还是很容易被GFW识别，这也就是为什么有的机场节点经常会出现不稳定现象，或者干脆就被封不能用了。而且公网传输，使用人多，流量拥挤就会速度变慢。<br>
好点的机场主可能会单独购买一条线路，这也就是我们说的独享线路机场，速度还稍微快点。有些功利性的机场主会租一条线路，意味着这一条线路同时被租给N个机场，这是我们常说的共享线路机场，速度和稳定性就得碰运气了。
* 公网中转（BGP中转）<br>
  * 用户 -> ss、ssr等协议 -> 国内中转服务器 -> 公网穿过GFW ->  国外服务器<br>
中转服务器到GFW这一段，一般会使用一些隧道协议，以实现负载均衡、高可用、防止被墙等效果，且对传输速度也做了优化。但是加BGP中转是比较昂贵的，所以能发现机场中带BGP中转的节点价格会比普通节点的价格贵。
* 专线内网中转（IPLC）<br>
  * 用户 -> ss、ssr等协议 -> 专线服务器A（自带中转功能）-> 内网传输 -> 国外专线服务器B<br>
这种方式你会发现，少了一个环节，就是它没有过GFW，就是传说中的不会被墙，因为它压根就不过墙，而且是点对点直接传输，速度也是快的。但是加IPLC比加BGP的价格更对，所以你会发现，机场节点中带IPLC的是卖的最贵的。目前国内大多的IPLC线都是采用的阿里内网线路，严格来说，不能算的上真正的IPLC。也有真正的IPLC线路，比较少，从商人角度来说，除非能回本儿，否则搞真正的IPLC是不划算的。[回到顶部](#readme)
#### 主观层面
除了技术层面，我们选择一个机场就是靠我们的主观判断，我个人是从以下几个方面判断的，只能供大家参考，不是绝对正确，毕竟这个行业鱼龙混杂，只要不怕担风险，是个人就可以开机场去捞金，水也较深。<br>
##### 机场的外观设计
大家会发现，几乎所有机场的界面布局都长得差不多，那是因为99%的机场用的模板代码都是同一套代码，细心的话，进机场的网站，看右下角（一般在右下，也有可能在左下），都有个staff的标志，没有staff的，会有SSPANEL，点进去也会看到staff。所以怎么去设计更换更精美的皮肤，也能侧面反映出机场主的用心程度。
##### 机场电报群观察交流
大多数的机场都会提供电报群链接，机场主一般也会在里边，购买前可进电报群，肯定会有用过的人对机场的优点问题等进行交流，也可从机场主日常在群中的活跃程度、答疑解惑、日常交流等方面去感受一个机场主是否真正用心在建设这个机场。<br>
##### 机场的测速
有些机场有试用，可试用测速。但个人建议测速的话，可以先尝试按流量去购买机场的服务，一般1G也就不到1元，管够测速使用了。这里建议测试分多个时间段去测，再把每个时间段的测速结果去做个平均，看是否满足你心理预期。多数人喜欢用YouTube测速，其实YouTube测速只能做个参考，想得到更精确的数据，还是用SPEEDTEST或FAST测，测速时候开启全局代理，把其它会走代理的程序全部关闭。[回到顶部](#readme)
##### 机场价格
这个其实不好评判，因为每个人心理的标准都不一样，个人感觉，只要体验感和机场的价格对称就行。没有哪个贵，哪个便宜之说，都是相对的。要根据自己的实际需求去购买，这跟咱们平时买车一样，好车就是体验好，但价格也不便宜。<br>

综述，个人认为主观方面的判断有时候可能比技术层面更重要，机场速度再快，再稳定，如果一段时间就跑路了，那还是掉坑了，所以我更看重主观层面的判断。因我自己也买过跑路的机场，身边很多朋友、网友也跟我说被坑过，所以非常看重这方面。[回到顶部](#readme)
## 我的[机场](https://stc-spades-beta1.com/auth/register?code=9JIx)使用感受<br>
* SSR、V2ray机场：STC，[官网](https://stc-spades-beta1.com/auth/register?code=9JIx)<br>
[STC机场](https://stc-spades-beta1.com/auth/register?code=9JIx)用了将近一年多，随着机场的几次升级，给我的体验感也由一般过渡到还行再到现在的好。也跟机场主聊过，去提一些建议，服务质量与价格还算对等。看YouTube4K视频、Netflix等视频网站没有任何问题。也可以去看一下[毒药大佬关于STC的测评](https://www.duyaoss.com/archives/1673/)。<br>
* Trojan机场：shadowsocks，[官网](https://portal.shadowsocks.nl/aff.php?aff=28409)<br>
原来的老牌shadowsocks机场，在2020年2月份所有节点全部升级为Trojan，也是为了规避GFW，目前机场的名字还叫shadowsocks。这个机场我是从2015年开始使用，升级之后速度和稳定性都有了很大提升。<br>
* 综合使用感受<br>
我是用的移动300M宽带，平时翻墙会看Netflix和YouTube多点，而且经常会下载一些视频资源，两个机场配合使用完全能满足我的日常需求，用起来的区别就是：<br>
  * 在一些高峰时段，Trojan机场看YouTube4K偶尔会出现卡顿，STC很少出现这种情况。<br>
  * 下载视频时候，STC是完全秒杀Trojan机场的，STC的下载速度能达到8M~12M,但Trojan机场的下载速度只有1M多。<br>
  * 当然STC的价格也比Trojan机场的价格高出很多。STC的基础套餐`每月38元`，还有其它的更高等级套餐，可自行到官网查看。Trojan机场的价格是`每年19.95AUD`（按现在汇率折合人民币86元）<br>
  
[回到顶部](#readme)
***

# 三、主流科学上网工具下载(包含Win、Mac、Android三大平台)
## Shadowsocks（简称SS）
* [Shadowsocks（Win）](https://github.com/shadowsocks/shadowsocks-windows/releases)<br>
* [Shadowsocks（Mac）](https://github.com/shadowsocks/ShadowsocksX-NG/releases/)<br>
* [Shadowsocks（Android）](https://github.com/shadowsocks/shadowsocks-android/releases)
## ShadowsocksR（简称SSR）
* [ShadowsocksR（Win）](https://github.com/shadowsocksrr/shadowsocksr-csharp/releases)<br>
* [ShadowsocksR（Mac）](https://github.com/qinyuhang/ShadowsocksX-NG-R/releases)<br>
* [ShadowsocksR（Android）](https://github.com/shadowsocksrr/shadowsocksr-android/releases)<br>
[回到顶部](#readme)
## V2ray（简称V2）
* [V2ray官方使用手册](https://www.v2ray.com/)
* V2ray的Windows端图形界面工具V2RayW和V2RayN
  * [V2RayW](https://github.com/Cenmrev/V2RayW/releases)<br>
  * [V2RayN](https://github.com/2dust/v2rayN/releases)<br>
* V2ray的Mac端图形界面工具V2RayX和V2RayU
  * [V2RayX](https://github.com/Cenmrev/V2RayX/releases)<br>
  * [V2RayU](https://github.com/yanue/V2rayU/releases)<br>
* [V2ray（Android）](https://github.com/2dust/v2rayNG/releases)<br>
[回到顶部](#readme)
## clash
* [clash（Win）简称CFW](https://github.com/Fndroid/clash_for_windows_pkg/releases) <br>
* [CFW使用说明书](https://docs.cfw.lbyczf.com/)
#### Clash.for.Windows汉化版，支持SSR和V2订阅
特别说明：官方的Windows客户端是英文，且只支持SS、Vmess、socks5和HTTP协议，这里有一个大神编译的汉化版本且支持SSR和V2ray的订阅<br>
[Clash.for.Windows-0.8.5汉化版](https://www.lanzous.com/i9zpaji)<br>
* [clash（Mac）](https://github.com/yichengchen/clashX/releases)<br>
* [clash（Android）](https://github.com/Kr328/ClashForAndroid/releases)<br>
[回到顶部](#readme)
## Trojan
* [Trojan-Qt5(Win+Mac)图形界面工具](https://github.com/TheWanderingCoel/Trojan-Qt5/releases)
* [Trojan-Qt5（Android）](https://www.lanzous.com/ia7vbhg)
* [Trojan的Windows、macOS、Linux三大平台命令行工具](https://github.com/trojan-gfw/trojan/releases)<br>
[回到顶部](#readme)
## Mellow
Mellow 是一个基于规则的全局透明代理工具，可以运行在 Windows、macOS 和 Linux 上，也可以配置成路由器透明代理或代理网关，支持 SOCKS、HTTP、Shadowsocks、VMess 等多种代理协议。<br>
* Mellow的[Windows、macOS和Linux安装文件下载](https://github.com/mellow-io/mellow/releases)<br>
[回到顶部](#readme)
## Netch
Netch是一个开源游戏加速器。与需要添加规则以用作黑名单代理的SSTap不同，Netch更类似于SocksCap64，后者可以扫描游戏目录以专门获取其进程名称并通过代理服务器转发其网络流量。现在支持Socks5，Shadowsocks，ShadowsocksR，VMess。<br>
同样，Netch避免了由SSTap引起的受限NAT问题。您可以使用NATTypeTester来测试您的NAT类型。当使用SSTap加速某些P2P游戏连接或该开放式NAT类型需要游戏时，您可能会遇到一些不好的情况，例如无法加入游戏。<br>
* [Netch下载](https://github.com/NetchX/Netch/releases)<br>
[回到顶部](#readme)
## Pharos Pro
* [Pharos Pro(Android)](https://github.com/PharosVip/Pharos-Android-Test/releases)<br>
* Pharos Pro(iOS)，登录非大陆AppleID下载。<br>
[回到顶部](#readme)
***

# 四、其它实用资源、工具
* [国际版抖音TikTok破解版iOS](https://www.lanzous.com/iaiv87e)<br>
* [国际版抖音TikTok破解版Android](https://www.lanzous.com/iaiv17c)<br>
* [Android短信轰炸机(付费版)](https://www.lanzous.com/s/sxcool1024)
* 手机影视三大神器，摆脱爱奇艺、优酷、腾讯平台的广告骚扰和会员限制：[小小影视永久官网](http://www.wangdunwen.com/?inviteCode=ID3WVM)、[南瓜影视永久官网](https://ng33.app/?channelCode=share?appkey=ayo1id&recommend=20965059)、[冬瓜影视永久官网](https://dg77.app/?channelCode=share?appkey=zphsu3&recommend=4897090)<br>
* 黑鸟视频播放器[官网](https://guihet.com/blackbird-player.html)（自带直播源，持续更新，只有Windows版）<br>
* 百度云盘搜索工具[下载地址](https://www.lanzous.com/i9wiekd)，六个搜索引擎，搜索整个百度云库，急速高效，自带提权码。<br>
* 百度网盘文件下载工具pandownload[官网](https://pandownload.com/)。<br>
* [草榴官网（需科学上网）](http://t66y.com/index.php?u=297138&ext=e4669)<br>
* [草榴Android下载地址](https://github.com/yuuwill/1024app-android/releases)<br>
* [草榴iOS下载地址](https://github.com/yuuwill/1024app-ios/releases)<br>
* [91app安装地址](http://app.91porn005.me:2082/aff-afeFw)<br>
* [iPhone通过快捷指令下载YouTube、Twitter视频](https://twitter.com/sxcool1024/status/1236090141606694912?s=20)<br>
[回到顶部](#readme)
***

`关于iOS平台的科学上网工具，目前支持协议较完善的有shadowrocket、suerge、Quantumult、Pharos等，需要用非大陆AppleID下载且收费，请大家自行注册购买`
# 欢迎加入电报群一起交流，群内每月会赠送草榴邀请码： https://t.me/sxcool1024g




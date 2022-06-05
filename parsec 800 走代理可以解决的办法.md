800报错

无法连接官方服务器 一般为无法直接访问网页和80/443端口

具体原因不知、大部分为移动或者部分电信联通

# **一.错误代码 800**

## **1. 找一个可以直接打开的代理**

也就是科学上网工具

（不需要流量很多网速很快、只能可以用就行，串流是不走代理的流量的）

我们只是需要他来登录、发现主机而已；串流依旧走的是P2P直连或者内网穿透。

没有代理的朋友可以下载群文件这个，之后自己注册账号然后测试web端

（免费的凑合能用，但不好用、时不时可能还会报错800.建议花钱找个靠谱的）

![](https://p3-juejin.byteimg.com/tos-cn-i-k3u1fbpfcp/b826ce9e2e3b4c36bb5587987d3cac83~tplv-k3u1fbpfcp-zoom-1.image)

**便宜代理的一个传送门：**

https://9.234456.xyz/abc.html（群友发的，我没用过不做评价和售后）

## **2.务必测试web端（这一步没有操作的、问我也没用）**

测试可以通过代理上

<https://web.parsec.app>（主要是这个）

<https://youtube.com>

可以正常打开登录

## **3.查看代理软件用的端口号**

（为parsec客户端直接使用代理做准备）

**Windows-系统代理直接查看：**

开始菜单搜索代理服务器

![](https://p3-juejin.byteimg.com/tos-cn-i-k3u1fbpfcp/d79120be136648eeb208af0911b40aa2~tplv-k3u1fbpfcp-zoom-1.image)

一般软件代理成功后会修改配置-就是我圈的那些

![](https://p3-juejin.byteimg.com/tos-cn-i-k3u1fbpfcp/46f46c4c2dbf47e79a7cd7531f94194f~tplv-k3u1fbpfcp-zoom-1.image)

连接时，肯定是打开的状态

提前编辑好以下：

app_proxy_address = 127.0.0.1

app_proxy_scheme = http

app_proxy = true

app_proxy_port = 7890

(每个软件不一样，不是都用7890)

**不要照抄我的、不要照抄我的、不要照抄我的、**

## **4.代理软件的端口到底怎么写（遇到理解错误最多的）**

1看 2改

### **例子1：**

![](https://p3-juejin.byteimg.com/tos-cn-i-k3u1fbpfcp/b3b68c84fd1649298acd5437f59b667e~tplv-k3u1fbpfcp-zoom-1.image)

app_proxy_address = 127.0.0.1

app_proxy_scheme = http

app_proxy = true

app_proxy_port = 7890

就这么写

### **例子2：**

![](https://p3-juejin.byteimg.com/tos-cn-i-k3u1fbpfcp/d4fdadb8037b49b58302e815e43d40b8~tplv-k3u1fbpfcp-zoom-1.image)

app_proxy_address = 127.0.0.1

app_proxy_scheme = http

app_proxy = true

app_proxy_port = 11000

说到底就是显示多少改成多少

### **例子3:**

![](https://p3-juejin.byteimg.com/tos-cn-i-k3u1fbpfcp/1c871869656343d4b96a1306ebd8d025~tplv-k3u1fbpfcp-zoom-1.image)

app_proxy_address=127.0.0.1

app_proxy_scheme=http

app_proxy=true

app_proxy_port=19180

### **例子4：**

![](https://p3-juejin.byteimg.com/tos-cn-i-k3u1fbpfcp/ec1ce3767cec4fa7991279f93524715d~tplv-k3u1fbpfcp-zoom-1.image)

app_proxy_address=127.0.0.1

app_proxy_scheme=http

app_proxy=true

app_proxy_port=4780

## **5.parsec客户端配置走代理线路**

说明：

由于parsec的特殊原因、他不能直接引用电脑上运行的代理软件。

需要我们手动写参数到该软件的配置文件中去。

**可直接看着两个，理解能力强直接往下看**

图文版

<https://www.bilibili.com/read/cv16937416>

视频版

<https://www.bilibili.com/video/BV1WU4y117iV/?spm_id_from=333.788>

**已登录过：**

访问您的高级设置（齿轮点进去拖到最底下选择最长的蓝色字母）

您可以在 Parsec 的设置中访问配置文件，滚动到底部并单击“直接编辑配置文件”。这些在除 Android 之外的所有平台上都可用。

或者，您可以在系统文件中找到 config.txt：

**未登录：**

Windows每个用户安装：%appdata%\Parsec\config.txt

共享安装：%programdata%\Parsec\config.txt

macOS / Linux / 树莓派：~/.parsec/config.txt

![](https://p3-juejin.byteimg.com/tos-cn-i-k3u1fbpfcp/e492da5dba9246a3ab2bbe2f79c00b66~tplv-k3u1fbpfcp-zoom-1.image)

（如果用户名是中文的朋友会在这里遇到报错、显示隐藏文件按照路径去找）

以我为例：C:\Users\admin\AppData\Roaming\Parsec 到这个文件夹再去找config.txt

————————————————————————————————————

**（自己具备代理的情况下、填写IP地址和端口以自己代理软件信息为准）**

**（自己具备代理的情况下、填写IP地址和端口以自己代理软件信息为准）**

**（自己具备代理的情况下、填写IP地址和端口以自己代理软件信息为准）**

app_proxy_address = 127.0.0.1

app_proxy_scheme = http

app_proxy = true

app_proxy_port = 7890

端口别抄了，自己是好多写好多

![](https://p3-juejin.byteimg.com/tos-cn-i-k3u1fbpfcp/fa20aa8aa9b14918889f846172112ee1~tplv-k3u1fbpfcp-zoom-1.image)

以上操作做完以后、点击parsec右下角图标右键重启

![](https://p3-juejin.byteimg.com/tos-cn-i-k3u1fbpfcp/52310dea81c04e1582a8e70c4d1db7bb~tplv-k3u1fbpfcp-zoom-1.image)

等待奇迹出现：

![](https://p3-juejin.byteimg.com/tos-cn-i-k3u1fbpfcp/6c524b52463942f29af82f299e7f7370~tplv-k3u1fbpfcp-zoom-1.image)

______________________________________________________________

# **二.错误代码6023（这个视频很多就不细说了）**

直说就是：你的网络不能被直接访问、需要用VPN或者内网穿透的方式来实现

多半为没有公网IP的情况下遇到。

组网之后务必ping一下对端ip地址看一下延迟

走转发 还是延迟高 100ms + 体验不好

如果走P2P 延迟会很低 10-40ms 体验好

（无论如何都延迟高、建议放弃）

## **1.通过蒲公英来搭建虚拟局域网实现连接**

<https://pgy.oray.com/download/personal/#visitor>

<https://service.oray.com/question/4970.html>

按照官方指引搞定了就去连接试一下

还不行就换别的

## **2.通过****Tailscale 在组网**

<https://sspai.com/post/66822>

Tailscale属于一种虚拟组网工具，基于WireGuard。

他能帮助我们把安装了Tailscale服务的机器，都放到同一个局域网。也就是我在家里的NAS和PC，还有父母家的PC，甚至云服务器都能放到同一个局域网。

## **3.通过Zerotier 来组网**

（不太推荐、虽然能用但是丢包严重抖动大，挣扎一下的试试）

<https://my.zerotier.com/network>

使用方法很多自己搜一下视频

## **4.如果双端都有ipv6，打开就可以、**

可通过该网址学习<https://ipw.cn/ipv6/> 或测试

# **三.其他问题：**

## **提问1：代理需要一直挂着？**

**不影响其他软件的时候建议一直挂着就可以，串流不会走代理的数据。**

代理的作用只是帮助你登录到服务器、告知另一端你在线罢了、

串流成功后：可以关闭代理软件 一般不影响串流。但仅限每次连接。

原则上：代理影响的是登录状态，不影响串流服务。关了就会报错800

## **提问2：有免费的代理吗？**

**个人认为免费基本是不靠谱的、建议找包月付费的比较便宜的那种**

我自己用的是比较贵的因为有其他用户就不推荐了

群公告放了两个链接，大家自己去找、或者问问其他群友

## **提问3：用了代理还是老出现800 卡顿**

如何测试自己的代理质量<https://fast.com/#> 看下延迟和速率吧

个人认为延迟100以内、速率有个10M左右差不多，主要看延迟。

![](https://p3-juejin.byteimg.com/tos-cn-i-k3u1fbpfcp/bd88e611d05545f88fcb35b8f9be7e10~tplv-k3u1fbpfcp-zoom-1.image)

## **提问4：为什么我照着视频设置完了还是不行**

1.  只是下载了代理客户端没有可出国的线路，所以白搭

<!---->

2.  没有先测试网页端和海外网站，这个东西不是写几个参数那么简单。

<!---->

3.  端口完全照着视频写了、但自己用的代理软件是别的端口，解决办法看 提问4.

<!---->

4.  同时开了两个代理软件，代理A可用代理B不可用，正好配置参数写的代理B。

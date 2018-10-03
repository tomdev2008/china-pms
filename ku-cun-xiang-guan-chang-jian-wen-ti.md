---
description: 库存管理至关重要，而牵涉到库存，又有非常多种原因需要逐一排查。为此，我们给出建议的自检步骤，可以根据以下方法进行自查，可以100%解决库存问题。
---

# 库存&新店上线相关问题

## 新酒店刚上线，你需要检查的事情有哪些？

{% hint style="success" %}
酒店是否已经被激活？
{% endhint %}

收到运营卫士的PMS账号密码≠PMS已经可以登录。如酒店未被激活，PMS是无法登陆，也就无法查看库存。

如果通过CRS搜酒店的PMS账号（如cn\_szx125）无法搜到，该酒店就是未激活。

如已经可以搜到，而PMS仍然无法登陆，可以通过进入CRS的酒店详情页检查酒店状态。

![&#x8FDB;&#x5165;CRS&#x9152;&#x5E97;&#x8BE6;&#x60C5;&#x9875;&#x67E5;&#x770B;&#x9152;&#x5E97;&#x72B6;&#x6001;&#x7684;&#x65B9;&#x6CD5;](.gitbook/assets/20181001_160106.gif)

  
Active酒店的特征：

* [x] 详情页OYO Status of Hotel后为active
* [x] 下拉看到 Multiple room category enabled后为true

{% hint style="success" %}
CRS权限是否已经完成设置？
{% endhint %}

如果酒店已经active了，PMS房态图无法显示，且首页显示如下图所示：

![&#x9996;&#x9875;&#x663E;&#x793A;&#x5982;&#x56FE;&#xFF0C;&#x623F;&#x6001;&#x56FE;&#x65E0;&#x6CD5;&#x5237;&#x65B0;](.gitbook/assets/image%20%289%29.png)

请检查酒店是否CRS权限完成设置，方法如下：

  


![&#x8FDB;&#x5165;CRS&#x9152;&#x5E97;&#x8BE6;&#x60C5;&#x9875;&#xFF0C;&#x67E5;&#x770B;Tags&#x662F;&#x5426;&#x6709;&#x5982;&#x4E0A;&#x56FE;&#x6807;&#x7B7E;](.gitbook/assets/20181001_160805.gif)

  
**如果没有看到标签，请邮件至&lt;techsupport@oyohotels.cn&gt;**催办理CRS的tag设置，标签出现后即可正常使用PMS。

{% hint style="success" %}
酒店tags已经正常了，还是出现以上情况，怎么回事？
{% endhint %}

检查一下Rooms是否有同步，方法如下：

![&#x5728;CRS&#x9152;&#x5E97;&#x8BE6;&#x60C5;&#x9875;&#x70B9;&#x51FB;Rooms&#xFF0C;&#x53D1;&#x73B0;&#x91CC;&#x9762;&#x6CA1;&#x6709;&#x4FE1;&#x606F;&#xFF0C;&#x4E0E;RoomInfo&#x4E0D;&#x4E00;&#x81F4;](.gitbook/assets/20181001_175537.gif)

  
解决方式依旧是**邮件联系&lt;techsupport@oyohotels.cn&gt;**协助

{% hint style="success" %}
Active酒店，标签设置完善，单独是显示库存不足无法录入
{% endhint %}

这个方法适用于不点选 Real Inventory \(Without Clubbing\) 查看酒店库存，全部显示为0的情况。

注意，它并不解决以下问题：

* 酒店超售（实际录入库存大于酒店总房间数）
* orbis或氪系统判断为黑房，无法售卖

刷新方法的在线视频教程如下：

{% embed data="{\"url\":\"http://v.youku.com/v\_show/id\_XMzgyMDgwOTcxMg==.html?spm=a2h1n.8251843.playList.5!9~5~A&f=51890881&o=1\",\"type\":\"video\",\"title\":\"10新建订单发现库存不足如何处理\",\"icon\":{\"type\":\"icon\",\"url\":\"http://static.youku.com/v1.0.166/index/img/favicon.ico\",\"aspectRatio\":0},\"thumbnail\":{\"type\":\"thumbnail\",\"url\":\"https://vthumb.ykimg.com/054104085B98BD6A00000170320109A1\",\"width\":448,\"height\":252,\"aspectRatio\":0.5625},\"embed\":{\"type\":\"player\",\"url\":\"//player.youku.com/embed/XMzgyMDgwOTcxMg==\",\"html\":\"<div style=\\\"left: 0; width: 100%; height: 0; position: relative; padding-bottom: 62.5%;\\\"><iframe src=\\\"//player.youku.com/embed/XMzgyMDgwOTcxMg==\\\" style=\\\"border: 0; top: 0; left: 0; width: 100%; height: 100%; position: absolute;\\\" allowfullscreen scrolling=\\\"no\\\"></iframe></div>\",\"aspectRatio\":1.6},\"caption\":\"刷新库存的教学视频\"}" %}

  
也可以参考以下动图：

![&#x5237;&#x65B0;&#x5E93;&#x5B58;&#x52A8;&#x56FE;&#x6559;&#x5B66;](.gitbook/assets/shua-xin-ku-cun.gif)

{% hint style="info" %}
新上线酒店房型和实际不一致怎么办？
{% endhint %}

PMS的房型信息是读取自CRS的Room Info的，查看Room Info的方式如下：

![&#x70B9;&#x51FB;Room Info&#x67E5;&#x770B;&#x9152;&#x5E97;&#x623F;&#x578B;&#x4FE1;&#x606F;](.gitbook/assets/20181001_164922.gif)

  
如CRS房型信息与签约不一致，请联系当地TR协助处理

## 已上线酒店，存在库存问题如何解决？

可以根据以下情况进行排除：

{% hint style="success" %}
是否存在OTA预抵订单未处理？是否存在当日应退房未及时操作？
{% endhint %}

PMS执行以下逻辑：

* 不支持超售，任何订单新建的时候都需要校验库存，库存不满足则无法建单
* OTA的订单在预抵状态就会占用酒店库存
* 在住订单只有在离店之后才会释放该房型的库存

所以如果存在OTA预抵订单占库存，或者当日应退房未及时处理，均会提示库存不足。

解决方案就是尽快准确处理订单，释放库存。

{% hint style="success" %}
是否存在入住房型和预定房型不同的情况？
{% endhint %}

目前在线的1.3.6存在一个bug（预计更新到1.3.7版后即可彻底解决），即更换房型后新房间不占库存，原房型不释放库存。

过渡解决方案如下：

1、新建订单换房型：

新建订单的时候，选择任意还有库存的房型，录入客人姓名和手机号

2、按实际入住情况选房：

在建好的订单下，根据客人实际入住情况，选择对应的房间号，房价按实际入住的房价录入

3、提醒前台尽可能建单时信息录入准确：

尽量安排客人，订什么房，住什么房；这样使用房态图直接建入住单的功能才能彻底正常使用。

{% hint style="success" %}
库存出现负值，订单无法录入
{% endhint %}

#### CRS存在两种库存计算方式。 {#kun-cun-ji-suan}

#### 一种是虚拟库存，是考虑房型升级的逻辑基础上的库存数。如标准大床房10间，行政大床房10间，标准大床房可以升级到行政房卖。在CRS上查看虚拟库存时，库存会显示标准大床房为20间。

#### 另一种是房型库存，房型库存是真实库存，是通过勾选 Real Inventory \(Without Clubbing\)后查看的。

![&#x70B9;&#x51FB;Real Inventory\(Without Clubbing\)&#x67E5;&#x770B;&#x9152;&#x5E97;&#x771F;&#x5B9E;&#x7684;&#x623F;&#x578B;&#x5E93;&#x5B58;](.gitbook/assets/image%20%286%29.png)

  
库存出现负值多是因为虚拟库存的原因，让部分房型超售。

在此时如无法在对应房型创建新单，只需要及时处理离店即可。

{% hint style="info" %}
泰坦PMS在1.0并不支持预排房功能，故库存满只能将现有库存清除后才能录单
{% endhint %}

{% hint style="success" %}
可售卖的库存比酒店实际的库存要少
{% endhint %}

查看酒店的可售卖房库存数据，可以通过查看CRS的RoomInfo实现，方法如下：

![&#x70B9;&#x51FB;Room Info&#x67E5;&#x770B;&#x9152;&#x5E97;&#x623F;&#x578B;&#x4FE1;&#x606F;](.gitbook/assets/20181001_164922.gif)

如酒店存在黑房，会体现在RoomInfo的Black Rooms里。

黑房有两种来源，一个是orbis系统，一个是氪系统。

如氪任务未完成，完成氪任务即可黑房变绿房在CRS里成为有效库存；

如氪任务完成或无氪任务，仍然有黑房，请联系TR团队协助检查PSA协议设置。

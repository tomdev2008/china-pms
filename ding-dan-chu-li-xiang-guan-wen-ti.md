# 订单处理相关问题

##  订单没有同步怎么办？/前台告诉我没有操作PMS但是订单状态变了怎么办？/订单状态变了但是房态图看不到？/订单状态变了，但是我没在PMS里操作，怎么回事？

迁移版PMS的本质是CRS信息的同步展示。所以在CRS里有的订单一定在PMS里是有的。

如果前台反映订单在CRS里能查到，而PMS里没有查到，大多数情况是他们没有找到订单的正确状态。比如在预抵订单中是查不到取消订单的。

核实方法是：

a.先通过CRS确认订单的状态

b.根据CRS里订单的对应状态，去PMS里查询对应订单

订单的状态变化有两种方式可以影响，一个是PMS修改，一个是客服在CRS里修改。如客服未规范操作，在CRS里直接修改订单状态而未分房，就会导致订单状态修改切房态图无法查询。

首先，查询订单操作日志。

方式如下图：

![&#x4F7F;&#x7528;CRS&#x67E5;&#x8BE2;&#x8BA2;&#x5355;&#x64CD;&#x4F5C;&#x65E5;&#x5FD7;](https://images-cdn.shimo.im/CD65l6Lkt80snKer/20180914_154632.gif)

客服的规范操作是，协助酒店办理check-in时，要求选择房型办理入住。不得直接切换订单状态。

**如检查出现有客服未选择房间号直接修改订单（history显示切check-in的不是酒店名称而是某个人名），就会出现房态图无法找到订单但是订单列表有客人信息的情况。**

## 怎么使用PMS查询订单？OTA订单取消了为什么PMS里还有？PMS取消的订单在CRS里是否可查询？

因为PMS是用预抵、在住、已完成、已取消、NoShow几种状态拆分的。

通常建议根据订单状态使用ctrl+f搜索订单。

如不确定订单状态，可以根据订单号在CRS里查询。查询方式见以下动图。

![&#x4F7F;&#x7528;CRS&#x901A;&#x8FC7;&#x8BA2;&#x5355;&#x53F7;&#x67E5;&#x8BE2;&#x8BA2;&#x5355;](.gitbook/assets/20180914_154632.gif)

因为目前PMS和OTA的直连非直接技术直连，中间存在操作延迟。如果有收到EBK发来的取消通知，前台需要录单，请打电话到客服申请加急订单取消处理。

CRS可以查到所有产生过的订单（包括取消订单），通过CRS搜索查找即可。  


## CRS库存被占满了（CRS库存为0），但房态图还有房，怎么回事？

有几种情况。

{% hint style="success" %}
客服未规范操作
{% endhint %}

我们首先捋一下CRS订单和PMS订单的逻辑。

对于任何一个酒店，有两种订单PMS进入PMS的方式，CRS和PMS。故订单的状态变化也有两种方式可以影响。

CRS的库存是通过统计当日店内处于check-in状态下的订单的总房间数来计算的。

而CRS里允许一种操作，即不分房可以直接修改订单状态，这就会导致CRS库存被占但房态图没有显示占房。原因是PMS的房态图是根据分房结果来呈现的。

如客服未规范操作，在CRS里直接修改订单状态而未分房，就会导致订单状态修改切房态图无法查询。

{% hint style="success" %}
种种原因换房
{% endhint %}

目前已知的线上bug是换房后CRS库存不改变，而新建订单校验的是酒店的[虚拟库存](https://oyo-china-pms-guideline.gitbook.io/taitan/~/edit/drafts/-LNsDEL9wWsM2hfZJEbQ/chan-pin-geng-xin-ri-zhi#kun-cun-ji-suan)\(点击查看定义），当房型虚拟库存用完后提示库存不足。

比如以下应用场景

例：OTA建单组发了3间豪华大床房今日入住的订单到PMS，因为酒店OTA名称不对，给过来的价格是住标准大床房的价格，前台按照标准大床房办理了入住

在这种情况下，CRS会显示豪华大床房库存扣减3间，而房态图会展现标准大床房入住3间。（房态图实际反馈了客人入住的情况，而CRS错误扣减了房型）

出现这种情况，建议走以下过渡解决方案：

1、新建订单换房型：

新建订单的时候，选择任意还有库存的房型，录入客人姓名和手机号，完成订单创建

2、按实际入住情况选房：

在建好的订单下，根据客人实际入住情况，选择对应的房间号，房价按实际入住的房价录入

3、提醒前台尽可能建单时信息录入准确：

尽量安排客人，订什么房，住什么房；这样使用房态图直接建入住单的功能才能彻底正常使用。

## OTA建单组提示我库存不足无法建单/OTA无法建单是为什么？

PMS执行以下逻辑：

* 不支持超售，任何订单新建的时候都需要校验库存，库存不满足则无法建单
* OTA的订单在预抵状态就会占用酒店库存
* 在住订单只有在离店之后才会释放该房型的库存
* PMS订单与CRS完全同步

简单说，如果酒店存在当日预离没有处理，库存占据着，OTA的订单是无法创建的。目前PMS并不支持预排房功能，而所有订单要求有库存才能录入。

处理方式为：尽快处理当日预离的订单，释放库存；如存在OTA订单取消，联系客服尽快操作取消

## OTA订单延迟，导致前台重复录单，或者前台按散客录单如何处理？

散客单的取消，分为几种情况：

* 散客订单录入后，仍在预抵状态：预抵状态的散客订单支持从PMS直接操作取消；
* 散客订单录入后，已办理入住：打电话到客服协助将散客单取消；

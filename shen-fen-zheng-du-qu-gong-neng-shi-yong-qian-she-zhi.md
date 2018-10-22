---
description: 泰坦支持使用酒店已有的身份证读卡器读取身份证信息，并存入系统。使用身份证读取功能之前，需要安装驱动，并变更chrome的flag服务设置
---

# 身份证读取功能使用前设置

## 身份证读取功能使用前设置

{% hint style="info" %}
读卡器驱动下载
{% endhint %}

泰坦PMS身份证读取驱动，支持80%以上酒店原有设备读取身份证信息。

使用右侧链接可下载驱动：[https://cdn.oyohotels.cn/plugin/OYOidCard.msi](https://cdn.oyohotels.cn/plugin/OYOidCard.msi)

下载后，请安装在您的电脑中。

{% hint style="info" %}
变更chrome的flag设置
{% endhint %}

如以下动画所示

在地址栏输入chrome://flags，回车

使用ctrl+f搜索“localhost”，选择对应的服务，将原有disable变成enable，变更后，点击"RELAUNCH NOW"重启浏览器。

![&#x4F7F;&#x7528;chrome&#x4FEE;&#x6539;localhost&#x6587;&#x4EF6;](.gitbook/assets/20180930_194859.gif)

## 身份证读取功能使用

{% hint style="info" %}
完成配置，在pms中读取客人身份证信息
{% endhint %}

读取成功，如下图所示：

![&#x70B9;&#x51FB;&#x65B0;&#x5EFA;&#x6563;&#x5BA2;&#x8BA2;&#x5355;&#xFF0C;&#x63D0;&#x793A;&#x201C;&#x6B63;&#x5728;&#x8FDE;&#x63A5;&#x8EAB;&#x4EFD;&#x8BC1;&#x8BFB;&#x5361;&#x5668;&#x670D;&#x52A1;&#x201D;](.gitbook/assets/image%20%2817%29.png)

{% hint style="danger" %}
如驱动已安装，读卡器连接失败，系统会提示“正在连接身份证读卡器服务”和“未识别到身份证读卡器，请检查设备是否连接”
{% endhint %}

![&#x5B89;&#x88C5;&#x9A71;&#x52A8;&#x6210;&#x529F;&#x672A;&#x8FDE;&#x63A5;&#x8BFB;&#x5361;&#x5668;](.gitbook/assets/image%20%2835%29.png)

泰坦在**新建订单时会自动启用身份证读卡器功能**。如在此次启动时，未能自动读取，可点击“启动身份证读卡器”再启动一次。

![&#x5982;&#x672A;&#x81EA;&#x52A8;&#x8BFB;&#x53D6;&#xFF0C;&#x53EF;&#x70B9;&#x51FB;&#x542F;&#x52A8;&#x8EAB;&#x4EFD;&#x8BC1;&#x8BFB;&#x5361;&#x5668;&#x542F;&#x52A8;&#x4E00;&#x6B21;](.gitbook/assets/image%20%285%29.png)

读取成功，客人的身份证信息会自动出现在系统中。如该客人此前有住过oyo酒店，则ta的手机号会自动出现在系统里。  


![&#x6210;&#x529F;&#x542F;&#x7528;&#xFF0C;&#x5E76;&#x5F55;&#x5165;&#x8BA2;&#x5355;&#x4FE1;&#x606F;](.gitbook/assets/image%20%2824%29.png)

{% hint style="danger" %}
泰坦1.3.7提供新的驱动安装包，安装后会在桌面自动建一个快捷方式，使用该快捷方式登录泰坦，无需设置localhost文件即可直接使用身份证读取功能
{% endhint %}

![&#x684C;&#x9762;&#x51FA;&#x73B0;OYO&#x6CF0;&#x5766;&#x5FEB;&#x6377;&#x65B9;&#x5F0F;&#xFF0C;&#x53CC;&#x51FB;&#x56FE;&#x6807;&#x5373;&#x53EF;&#x5FEB;&#x901F;&#x767B;&#x5F55;&#x6CF0;&#x5766;](.gitbook/assets/image.png)

## 身份证读卡器申领

如酒店无身份证读卡器或读卡器无法适配，可按照以下文件申请领用。

{% file src=".gitbook/assets/oyo-shen-fen-zheng-du-qia-qi-jian-ce-ji-ding-ding-shen-qing-liu-cheng-2.pdf" %}


---
description: 泰坦支持使用酒店已有的身份证读卡器读取身份证信息，并存入系统。使用身份证读取功能之前，需要安装驱动，并变更chrome的flag服务设置
---

# 身份证读取功能使用前设置

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

{% hint style="info" %}
完成配置，在pms中读取客人身份证信息
{% endhint %}

读取成功，如下图所示：

![&#x65B0;&#x5EFA;&#x8BA2;&#x5355;&#x9875;&#x9762;&#xFF0C;&#x5F00;&#x59CB;&#x8EAB;&#x4EFD;&#x8BC1;&#x8BFB;&#x53D6;](.gitbook/assets/image%20%288%29.png)

  


![&#x5982;&#x672A;&#x81EA;&#x52A8;&#x8BFB;&#x53D6;&#xFF0C;&#x53EF;&#x70B9;&#x51FB;&#x542F;&#x52A8;&#x8EAB;&#x4EFD;&#x8BC1;&#x8BFB;&#x5361;&#x5668;&#x542F;&#x52A8;&#x4E00;&#x6B21;](.gitbook/assets/image%20%285%29.png)

  


![&#x6210;&#x529F;&#x542F;&#x7528;&#xFF0C;&#x5E76;&#x5F55;&#x5165;&#x8BA2;&#x5355;&#x4FE1;&#x606F;](.gitbook/assets/image%20%2810%29.png)

{% hint style="danger" %}
泰坦1.3.7提供新的驱动安装包，安装后会在桌面自动建一个快捷方式，使用该快捷方式登录泰坦，无需设置localhost文件即可直接使用身份证读取功能
{% endhint %}

![&#x684C;&#x9762;&#x51FA;&#x73B0;OYO&#x6CF0;&#x5766;&#x5FEB;&#x6377;&#x65B9;&#x5F0F;&#xFF0C;&#x53CC;&#x51FB;&#x56FE;&#x6807;&#x5373;&#x53EF;&#x5FEB;&#x901F;&#x767B;&#x5F55;&#x6CF0;&#x5766;](.gitbook/assets/image.png)


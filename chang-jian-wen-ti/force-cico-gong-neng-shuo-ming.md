---
description: 强制入住与强制离店（10月23日上线）
---

# Force CI/CO功能说明与补录问题

##   Force C/I

###         i.          NoShow功能

在订单入住日次日的上午6:00~11：55，订单出现**NoShow按钮**，点击“NoShow”后订单状态修改为NoShow

在上午**11:30在PMS界面上提示系统通知：“30min后，昨天未入住订单将被系统默认入住，请尽快处理”**

###        ii.          订单check in

订单入住日次日**中午12:00前，可以操作订单的入住，可以创建前一日订单进行补单。**12：00之后，无法补单及补入住。

###       iii.          Force C/I

订单入住日次日中午12:00后，如订单状态仍旧是预抵，则**状态修改为force Check-in**，由系统根据订单房型任意选择同房型任意房间入住，如果没有同类型房间，选择其他空房。押金金额为0。

![Force C/I&#x529F;&#x80FD;&#x8BF4;&#x660E;](../.gitbook/assets/image%20%2856%29.png)

![Force Checked In&#x6267;&#x884C;&#x540E;&#xFF0C;&#x5907;&#x6CE8;&#x680F;&#x51FA;&#x73B0;&#x5BF9;&#x5E94;&#x6807;&#x7B7E;](../.gitbook/assets/image%20%2825%29.png)

##  Force C/O

###   i.          正常C/O时间

在订单离店日当日下午18:00之前，所有订单允许通过交互正常离店。**不会出现force check out或无法离店的情况**。

###   ii.          Force C/O

订单离店日当日下午17:30，**提示“30min后，今日未离店订单将会被系统默认离店，如需续住，请尽快处理”**

订单离店日当日下午18:00以后，订单状态为预离的订单，系统自动办理离店。**订单上未付金额默认以现金收入，押金以收入的方式，原路退回**。

### iii． Force Tag

所有通过force功能切换订单状态的订单，有force标签，**可以追溯哪些订单是force CI或force CO的**

### iv． Force CI/CO 订单邮件通知

每天13:00，邮件通知Force CI的订单情况；每天19:00，邮件通知Force CO的订单情况；

**原pending状态由Force CI或Force CO替代**。

![Force C/O&#x529F;&#x80FD;&#x8BF4;&#x660E;](../.gitbook/assets/image%20%2841%29.png)

![Force Checked Out&#x6267;&#x884C;&#x540E;&#xFF0C;&#x5907;&#x6CE8;&#x680F;&#x51FA;&#x73B0;&#x76F8;&#x5E94;&#x6807;&#x7B7E;](../.gitbook/assets/image%20%2834%29.png)

## Force订单争议解决流程

### Force订单列表

Force C/I & C/O发生的当日，会出具force订单列表。

12：00出具Force C/I订单列表，18：00出具Force C/O订单列表。

### 订单异议审批

AGM可根据报表对订单提出异议，时间是报表出具日当晚的24：00未来3天。总部客服团队会根据CGM审批结果进行修改。

异议提出截止日是报表出具日后第三天的18：00。

![Force CI/CO&#x8BA2;&#x5355;&#x68C0;&#x67E5;&#x53CA;&#x4E89;&#x8BAE;&#x5BA1;&#x6279;](../.gitbook/assets/image%20%2829%29.png)

具体流程如下：

使用钉钉发起审批流程，在钉钉“工作”里找到“审批”，找到Force Check争议申请，点击进入。

![Force Check&#x4E89;&#x8BAE;&#x7533;&#x8BF7;](../.gitbook/assets/image%20%2867%29.png)

![&#x586B;&#x5199;&#x4E89;&#x8BAE;&#x7533;&#x8BF7;&#x4FE1;&#x606F;&#xFF0C;&#x9009;&#x62E9;&#x5BF9;&#x5E94;&#x57CE;&#x5E02;CGM&#x534F;&#x52A9;&#x7533;&#x8BF7;&#xFF0C;&#x70B9;&#x51FB;&#x201C;&#x63D0;&#x4EA4;&#x201D;&#x5373;&#x53EF;](../.gitbook/assets/image%20%2817%29.png)

  
附件模板：（下载填写后，使用“添加附件”上传到钉钉）

{% file src="../.gitbook/assets/ding-dan-zhuang-tai-zheng-yi-mo-ban.xlsx" %}

## 补录订单

泰坦1.0允许在订单入住日后一天12：00之前补录前一日订单。补录订单如有库存问题可[点这里](https://oyo-china-pms-guideline.gitbook.io/taitan/ku-cun-xiang-guan-chang-jian-wen-ti#yi-shang-xian-jiu-dian-cun-zai-ku-cun-wen-ti-ru-he-jie-jue)查看原因。


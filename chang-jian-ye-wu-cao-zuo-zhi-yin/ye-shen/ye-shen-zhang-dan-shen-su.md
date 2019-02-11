# 订单申诉

## 错误订单处理方法

### 状态错误需取消

| 渠道\订单状态 | 预抵 | 在住 | 离店 | Noshow |
| :---: | :---: | :---: | :---: | :---: |
| PMS | PMS直接取消 | PMS操作0房费当日入离 | 异常订单修改/取消申请 | 入住日次日12点往后48小时内进行noshow申诉操作 |
| OTA非直连 | 联系客服并提供取消凭证 | PMS操作0房费当日入离 | 异常订单修改/取消申请 | 现付noshow申诉，预付异常订单 |
| OTA直连 | 联系客人在OTA上取消 | 联系客人在OTA上取消 | 异常订单修改/取消申请 | 现付noshow申诉，预付异常订单 |
| OYO小程序&app | 联系客服 | PMS操作0房费当日入离 | 异常订单修改/取消申请 | 现付noshow申诉，预付异常订单 |
| MM | 联系对应销售 | PMS操作0房费当日入离 | 异常订单修改/取消申请 | 现付noshow申诉，预付异常订单 |

### 价格错误需修改

<table>
  <thead>
    <tr>
      <th style="text-align:center">渠道\订单状态</th>
      <th style="text-align:center">预抵</th>
      <th style="text-align:center">在住</th>
      <th style="text-align:center">离店</th>
      <th style="text-align:center">Noshow</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:center">PMS</td>
      <td style="text-align:center">直接在PMS上修改</td>
      <td style="text-align:center">房费调整</td>
      <td style="text-align:center">异常订单修改/取消申请</td>
      <td style="text-align:center">异常订单修改/取消申请</td>
    </tr>
    <tr>
      <td style="text-align:center">OTA非直连</td>
      <td style="text-align:center">联系建单组改价</td>
      <td style="text-align:center">房费调整</td>
      <td style="text-align:center">异常订单修改/取消申请</td>
      <td style="text-align:center">异常订单修改/取消申请</td>
    </tr>
    <tr>
      <td style="text-align:center">OTA直连</td>
      <td style="text-align:center">按原价入住</td>
      <td style="text-align:center">房费调整</td>
      <td style="text-align:center">异常订单修改/取消申请</td>
      <td style="text-align:center">异常订单修改/取消申请</td>
    </tr>
    <tr>
      <td style="text-align:center">OYO小程序&app</td>
      <td style="text-align:center">
        <p>与客人协商一致，</p>
        <p>入住后进行房费调整</p>
      </td>
      <td style="text-align:center">房费调整</td>
      <td style="text-align:center">异常订单修改/取消申请</td>
      <td style="text-align:center">异常订单修改/取消申请</td>
    </tr>
    <tr>
      <td style="text-align:center">MM</td>
      <td style="text-align:center">入住后进行房费调整</td>
      <td style="text-align:center">房费调整</td>
      <td style="text-align:center">异常订单修改/取消申请</td>
      <td style="text-align:center">异常订单修改/取消申请</td>
    </tr>
  </tbody>

# 异常订单修改

#### 申请流程

异常订单修改/取消申请由AGM发起，通过邮件发送错误订单明细及需要修改的信息至&lt;wrong\_order.cst@oyohotels.cn&gt;

![](../../.gitbook/assets/image%20%28173%29.png)

#### 邮件格式&修改时间

* 邮件格式

邮箱：wrong\_order.cst@oyohotels.cn

邮件主题：城市+酒店编码+OTA平台

邮件内容：平台订单号+宙斯订单号（选填）+修改订单原因

* 修改时间

每月1日-18日，修改1日-15日入住的订单

每月16日-次月2日，修改16日-月底入住的订单

* OTA处理时效

收到邮件后24小时内，回复邮件告知处理结果

## NoShow订单申诉

### 发起申诉

预入住日次日的12：00后的48小时内为noshow申诉时间。

如存在系统自动夜审产生的noshow与实际不符，需要取消，请在规定时间内及时申诉。

**如超过申诉时间，noshow状态会变成【申诉驳回，房单确认收入】**。

确认收入的订单，不再接受修改。

可以通过Titan的侧边栏【在住管理】-【在住列表】-【noshow申诉】界面进行noshow申诉。

![&#x8FDB;&#x5165;&#x7533;&#x8BC9;](../../.gitbook/assets/image%20%28133%29.png)

客服会在接到申诉的24小时内处理申诉。  


* 如申诉成功：订单状态会变成“申诉成功，房单取消”，该房单将不会进入抽佣范围；
* 如申诉失败：订单状态会变成“申诉驳回，房单确认收入”

该状态会是房单的**最终状态**。

### 申诉审批

发起申诉的24小时内：

* 客服进行申诉通过与申诉驳回操作
* 申诉通过的订单，在申诉处理界面，该房单转为“取消”，已生成的应收账单会被删除

![&#x7533;&#x8BC9;-&#x53D6;&#x6D88;](../../.gitbook/assets/image%20%28183%29.png)

* 申诉驳回的订单，订单状态变成“确认收入”，订单已产生及待产生应收，全部生成实收挂账进行平账，在驳回日之后所有订单剩余天数库存将被释放；

![&#x7533;&#x8BC9;-&#x786E;&#x8BA4;&#x6536;&#x5165;](../../.gitbook/assets/image%20%28260%29.png)

### 申诉超时

订单状态变成“待申诉”的48小时之后，如其中无申诉操作，订单状态由“待申诉”状态变成“**申诉驳回，房单确认收入**”，订单已产生及待产生应收，全部生成实收挂账进行平账处理，释放当前日期之后剩余天数库存。


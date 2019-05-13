# 夜审前/后需要做什么

## 夜审之前需要做什么？

根据以上变更，夜审前需要操作的事情也有所变化。

夜审之前，酒店需要处理以下事宜：

* 及时操作入住
* 及时操作离店
* 对未到店客人操作NoShow
* 对订单状态/金额/信息等不正确的订单发起申诉
* 确认每一个在住订单的金额

## 夜审之后需要做什么？

夜审时，所有的待入住订单都会切换为入住状态。

故夜审之后需要酒店处理以下事宜：

* 对系统自动入住、客人实际到店的订单补排房补入住人信息，保证房态准确。
* 对系统自动入住、客人实际未到店的订单进行申诉
* 对前一日金额错误的散客订单进行冲账
* 对前一日订单状态/金额/信息错误的订单进行申诉

## 什么都不做会发生什么？

如未操作订单，会发生以下事情：

* 待入住订单会变为入住状态，系统打上自动入住标记
* 系统自动入住会占据库存，但不会自动分房，所以房态图无法查到系统自动入住的订单
* 预离日时，在住状态会变为离店状态，系统打上自动离店标记
* 离店后2天的24：00之后，订单状态固化，生成预结账单，不再接受订单申诉

## 如何挽救？

对于所有自动入住/自动离店的订单，如未及时操作，会影响到佣金账单。

如需挽救，可以通过申诉功能来实现。申诉必须在预离日2天后的24：00之前完成。尽量在每日夜审之前完成申诉的检查，处理完当日的申诉。

![](../../../.gitbook/assets/image%20%28476%29.png)

申诉功能在变更后，支持以下问题类型

* 订单状态错误
* 预定来源错误
* 入账主体错误
* 渠道订单号错误
* 预订人姓名错误
* 预订人联系电话错误
* 预订单备注错误
* 订单价格错误
* 其他

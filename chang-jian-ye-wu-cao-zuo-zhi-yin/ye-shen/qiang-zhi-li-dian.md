# 自动离店

## 续住提示

目前未设计，如客人行李仍在房间内，或判断客人需要续住，请在18：00前及时操作续住。

系统在每日12：00之后会把当日预离订单打上超时标签，如下图所示：

![&#x8D85;&#x65F6;&#x6807;&#x7B7E;](../../.gitbook/assets/image%20%281029%29.png)

该续住只有到夜审时间时才会产生应收，如客人延期离店需要收费，请通过入账功能录入房费调整-延期离店。

## 自动离店

在每日18：00，查询当天应离未离的在住房单，其状态会有以下变化：

* 未平账房单挂账离店并打上自动离店标识（现阶段仅在数据库展示），房态改为脏房
* 已平账房单打上自动离店标识，房态改成脏房


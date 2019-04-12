---
description: 介绍夜审三期的改造
---

# 夜审改造（三期）

夜审三期改造，主要是引入了人工夜审环节，并修改了NoShow的逻辑。

下面会根据以下几个主题来做简单讲解：

* 有哪些改变，解决了什么问题？
* 夜审之前需要做什么？
* 夜审之后需要做什么？
* 什么都不做会发生什么？
* 如何挽救？

## 为什么要做夜审三期

夜审二期在夜审时，将所有订单切为NoShow，占据库存，会带来以下问题：

* 无法反馈酒店真实NoShow客源的情况，而NoShow订单率是酒店运营过程中重要考核指标，是收益定价的重要依据；
* 占据库存的NoShow订单不计算urn，造成occ数据不准确
* NoShow的现预付申诉分离，线上申诉功能不全，导致账单混乱

## 夜审三期做了哪些优化

* **自动NoShow变为手工NoShow：**酒店可以在入住日当日23：00~次日6：00之间，对未到店的客人标记NoShow
* **可使用人工NoShow的方式及时释放库存：**现阶段因NoShow状态的订单会占据库存，酒店在确认客人未到的时候，也无法将房间售卖，或实际售卖而无法录单。经夜审三期调整后，该问题将得到解决。
* **可实现订单的部分取消/NoShow：**现阶段因该功能缺失，销售和OP在操作团单的时候需要很多线下沟通，酒店不会将未来的团队订单录入系统，该情况会带来较高的到店无房风险
* **夜审时所有待入住订单变更为入住**：现阶段未及时操作的订单在夜审时会变成NoShow状态，该状态在统计URN时不会被计入。调整为自动入住后，URN将会被计入
* **新增申诉原因：**可以满足订单状态错误/信息错误/价格错误等多种类型的申诉
* **申诉时间变更：**从下单开始至离店日后2天内的24：00之前。截止后订单状态固化，不再更改
* **申诉流程简化，酒店账单会更准确**：现阶段NoShow申诉时间限制短，功能不全，大多数挤压的状态错误\金额错误订单只能通过线下邮件的方式解决，该方式下，OP工作量大且效率低下。 因效率低下，很多OP甚至不会进行调整，导致酒店账单不准确，造成OYO与业主关系紧张。 经夜审三期调整后，申诉流程大大简化，且覆盖了所有场景，酒店账单准确性大幅提高。
* **NoShow的数据会更精确的反馈酒店的运营情况：**现阶段所有NoShow仅为系统自动操作，无法区分出哪些客人是真实NoShow的哪些是前台不操作系统所导致的。 经夜审三期调整后，NoShow将回归其在酒店运营中的数据意义，从而可以协助CP/OP更好地进行收益分析，帮助酒店提升业绩。
* **CRS支持客服自行发起异常处理**

## 夜审之前需要做什么？

![](../.gitbook/assets/image%20%28581%29.png)

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

![](../.gitbook/assets/image%20%28354%29.png)

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

## 具体操作指引

### 待入住房单手工NoShow   

 [点击查看部分noshow/取消视频](http://crs-pms-vidio.oss-cn-beijing.aliyuncs.com/%E5%A4%9C%E5%AE%A1-%E9%83%A8%E5%88%86%E5%8F%96%E6%B6%88%26%E9%83%A8%E5%88%86noshow.mp4)

[点击查看noshow立即释放库存视频](http://crs-pms-vidio.oss-cn-beijing.aliyuncs.com/%E5%A4%9C%E5%AE%A1-noshow%E7%AB%8B%E5%8D%B3%E9%87%8A%E6%94%BE%E5%BA%93%E5%AD%98.mp4)

点击订单列表，通过今日预抵，进入办理入住页面

![](https://uploader.shimo.im/f/YcLjiFoDWSgOb0tD.png!thumbnail)

点击“noshow”并确认，该房单会变为noshow状态（另外两个房间仍然可以办理入住）

![](https://uploader.shimo.im/f/qjWNj0gz6Cs9v35I.png!thumbnail)

![](https://uploader.shimo.im/f/FWF9PeEwcSAHaQXO.png!thumbnail)

* noshow后，库存释放、房态释放

### 待入住房单手工取消

在办理入住页面，找到需要取消的房单，点击“取消房单”并确认即可。

![](https://uploader.shimo.im/f/rX4MBgx0KVUAsRb2.png!thumbnail)

取消成功后，原订单中的3间房会变成2间，且未操作noshow也未操作取消的房单仍然可以办理入住。

![](../.gitbook/assets/image%20%2884%29.png)

### 待入住订单手工noshow

[点击查看订单noshow视频](http://crs-pms-vidio.oss-cn-beijing.aliyuncs.com/%E5%A4%9C%E5%AE%A1-%E6%95%B4%E5%8D%95noshow.mp4)

点击订单列表，通过今日预抵，进入办理入住页面

![](https://uploader.shimo.im/f/TcwHb7SKZ3otrET6.png!thumbnail)

点击“订单信息”栏右上角的三个点，点击“noshow”并确认，可以将该订单下所有未入住的房单变为noshow状态

![](https://uploader.shimo.im/f/wHhKjW7YJQo7NjzI.png!thumbnail)

![](https://uploader.shimo.im/f/p2jRG5rdXwAHdZi2.png!thumbnail)

在全部订单中查看该订单状态，可以看到订单状态变为“noshow”

![](https://uploader.shimo.im/f/tKkr46lRY6g2A9iY.png!thumbnail)

### 待入住订单手工取消

可参考现有的订单取消流程。

进入办理入住页面，点击“订单信息”栏右上角的三个点，点击“取消订单”并确认，可以取消该订单。

![](https://uploader.shimo.im/f/MNpOYoBUxU0jhf8G.png!thumbnail)

在全部订单中查看该订单状态，可以看到订单状态变为“取消”

![](https://uploader.shimo.im/f/t8hHqfyyz2YGbeyd.png!thumbnail)

### 团单手工NoShow/取消

#### 团单中的房单noshow与取消

[点击查看视频](http://crs-pms-vidio.oss-cn-beijing.aliyuncs.com/%E5%A4%9C%E5%AE%A1-%E5%9B%A2%E5%8D%95%E9%83%A8%E5%88%86%E5%8F%96%E6%B6%88%26%E9%83%A8%E5%88%86noshow.mp4)

通过“订单列表”→“团单”→“团单入住”，进入到团单入住页面。

![](https://uploader.shimo.im/f/MgJ0VjN9PJk1ORJE.png!thumbnail)

单击排好的房间，下方会出现该房间信息。

![](https://uploader.shimo.im/f/RXdugErFfQsnOytd.png!thumbnail)

点击“noshow”并确认，即可noshow该房单。

![](https://uploader.shimo.im/f/QGyZdTF9LhMlAyq5.png!thumbnail)

![](https://uploader.shimo.im/f/JLUBsGrmwmQAnGv9.png!thumbnail)

点击“取消”并确认，即可取消该房单。 

![](../.gitbook/assets/image%20%28265%29.png)

![](https://uploader.shimo.im/f/xSNi07q76hojox4B.png!thumbnail)

#### 整个团单noshow与取消

整个团单的noshow与取消流程参考上面提到的在住订单noshow与取消。

## 夜审后相关操作指引

### 自动入住

夜审时，所有待入住订单变更为入住状态，在“在住列表”中可以查看到，此类自动入住的订单，没有房间号。

![](../.gitbook/assets/image%20%28405%29.png)

双击此条记录，跳转到在住详情页面，点击“日志”标签，可以查看到入住的操作人为：PMS系统

![](../.gitbook/assets/image%20%28133%29.png)

### 补排房/补入住人信息

系统自动入住的房间，如果确认客人确实到店，则需要进行补排房操作（保证房态准确），同时需要补录入住人信息。

找到需要补排房的订单，点击“排房”按钮

![](../.gitbook/assets/image%20%28598%29.png)

进入到入住页面，排房读取客人身份信息，确认入住即可。

![](../.gitbook/assets/image%20%28443%29.png)

![](https://uploader.shimo.im/f/Io67fKtnVpAYw1oK.png!thumbnail)

### 异常订单申诉

#### 申诉有效时间

订单的申诉有效期为：从下单开始，至离店日后2天内的24：00之前。

#### 申诉操作流程

[点击查看视频](http://crs-pms-vidio.oss-cn-beijing.aliyuncs.com/%E5%A4%9C%E5%AE%A1-%E6%8F%90%E4%BA%A4%E7%94%B3%E8%AF%89.mp4)

确认需要申诉的订单号并复制（如下图）

![](https://uploader.shimo.im/f/VJ8APXOvwnE9Ay3n.png!thumbnail)

点击页面悬浮框中的“申诉”按钮，跳转到申诉页面。

![](https://uploader.shimo.im/f/bEK8uMdxpNojbR50.png!thumbnail)

将需要申诉的订单号粘贴进去，并点击“校验订单号”，若订单号正确且订单在申诉有效期内，页面下方会出现申请操作区。

![](https://uploader.shimo.im/f/dXzDLa96W0wKvt5Y.png!thumbnail)

在下拉框中选择申诉的具体内容

![](https://uploader.shimo.im/f/twY67rFQ7fUYC5C4.png!thumbnail)

选择完成后，在弹窗的框中填写相关信息（选择不同的申诉内容，需要填写的信息也不同）

如选择订单号错误，则需要填写以下信息

![](https://uploader.shimo.im/f/JaTy1sV7RBYPqxaU.png!thumbnail)

点击“添加申诉原因”，可以添加订单的申诉原因

![](https://uploader.shimo.im/f/Ho0GraBSax0H45Bd.png!thumbnail)

如此次选择“联系电话错误”，则需要填写以下信息

![](https://uploader.shimo.im/f/yx4VpCK7SN4aAIWr.png!thumbnail)

申诉信息填写完毕后，点击右下角的“提交申诉”按钮即可

* 一个申诉批次里，每个申诉原因，只能提交一次
* 只有OTA非直连订单来源，才能切换成其他OTA非直连来源

#### 查看申诉列表

[点击查看视频](http://crs-pms-vidio.oss-cn-beijing.aliyuncs.com/%E5%A4%9C%E5%AE%A1-%E6%9F%A5%E7%9C%8B%E7%94%B3%E8%AF%89%E5%88%97%E8%A1%A8.mp4)

点击“在住管理”→“在住列表” 

![](../.gitbook/assets/image%20%2846%29.png)

点击“申诉”标签，即可进入申诉列表，可以查看申诉的详情及日志

![](https://uploader.shimo.im/f/SfJECtEPSYwF9itc.png!thumbnail)

![](https://uploader.shimo.im/f/rT4eL4WH8AYigO4I.png!thumbnail)

![](https://uploader.shimo.im/f/bSOwOD9zynoA9kvQ.png!thumbnail)




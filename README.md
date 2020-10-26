# -KDNIAO_JAVA_DEMO
## 前期准备工作
去[快递鸟官网](http://www.kdniao.com/reg)免费注册一个账号，免费获得一个apiKey(接口权限验证需要)，完成实名认证流程，订购一个免费或付费套餐（也可找快递鸟工作人员免费申请付费的接口测试联调）

注：登录快递鸟用户管理后台后获得用户ID和APIKey对应各demo中的EBusinessID、AppKey。

小知识：EBusinessID跟APIKey是什么？EBusinessID跟APIKey您在快递鸟网站注册之后快递鸟分配的密钥（对应官网上的用户ID和API key），用于保证应用来源的可靠性，避免应用伪造，被不法使用。


## 对接中的其他说明
1、物流查询（免费版）会员套餐为免费版，有效期1年结束后，如在近3个月内有数据交互系统会自动免费续期；

2、**即时查询（RequestType：1002/8001）**日查询次数<=3000次对接即时查询接口

3、请求接口之前需要先实名认证，开通相关会员服务，否则会请求失败并返回提示“未申请开通接口”；

4、接口开发可以下载“当前项目”更改KEY密钥；

5、**物流跟踪（RequestType：1008/8008）**日查询次数>3000次对接物流跟踪接口

6、测试订阅接口，对照技术文档正确返回代表订阅接口对接成功，详情可见技术文档。

7、开发推送接口，无demo提供，推送时会推送requestType、requestData和DataSign三个参数，您开发一个推送接口接收这三个参数就行，成功接收后需要在5S内给快递鸟返回成功收数据的报文，否则超时。RequestData中包含应用级参数，即物流轨迹（详情看技术文档）；

8、订阅接口、推送接口分别测试成功后，可使用正式地址进行订阅真实的快递单号，快递鸟一般会在2-12小时内推送物流信息至您已经配置好的回调地址上;

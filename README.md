# 微信群机器人

目前支持的功能：

* 在两个群中间转发文本，图片，自定义动画表情，链接。微信群有500人的容量限制，一个消息转发机器人可以通过把几个群接起来相互转发消息来突破这样的限制。
* 用正则表达式来自定义回复。
* 响应/tagcloud，生成整个群的标签云，或者响应/mytag，生成某个用户的标签云。
* 响应/activity，生成群的活跃度时间图，以及活跃用户饼图。
* 自动排队。如果群里出现了二传，自动三传。

目前不支持的功能：

* 转发表情商城中的表情（即使表情是免费的）
* 转发红包（想啥呢你）
* 多于两个群的转发（但更改应该很简单）

## 部署

* 运行`deploy.sh`。
* 依赖于[itchat](https://itchat.readthedocs.io/zh/latest/)

## 运行

* 这个小工具不是针对最终用户的，所以现在需要改code（main.py）来设置想要转发的群名。
* `python3 -u main.py`。会弹出一个二维码扫码登录。
* 如果在Linux VPS上运行，ssh进去的时候记得加上X转发，这样才能看到二维码。如果不用X转发的话也可以手工下载文件或者改用命令行二维码。

## 已知问题

* 如果启动时候说无法找到群，请在群里说句话。这是微信接口的限制所致。

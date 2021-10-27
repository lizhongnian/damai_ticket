#### 提前准备
* Python 3.6+
* Chromedriver.exe
* Chrome 浏览器安装好后需将chromedriver.exe放置于Chrome浏览器目录下
* pip install selenium

#### 参数设置

在`config.json`中输入相应配置信息，具体说明如下：

* `sess`: 场次优先级列表，如本例中共有三个场次，根据下表，则优先选择1，再选择2，最后选择3；也可以仅设置1个。
* `price`: 票价优先级，如本例中共有三档票价，根据下表，则优先选择1，再选择3；也可以仅设置1个。
* `real_name`: [1,2], 实名者序号，如本例中根据序号共选择两位实名者，根据序号，也可仅选择一位
  * 选择一位或是多位根据购票需知要求，
  * 若无需实名制信息则不需要填写，
  * 若一个订单仅需提供一位购票人信息则选择一位，
 * 若一张门票对应一位购票人信息则选择多位）。
 
* `nick_name`: 用户在大麦网的昵称，用于验证登录是否成功
* `ticket_num`: 购买票数
* `damai_url`: https://www.damai.cn, 大麦网官网网址
* `target_url`: https://detail.damai.cn/item.htm?id=599834886497  目标购票网址

* 部分门票需要选择城市，只需选择相应城市后将其网址复制到config.json文件的target_url参数即可。

* 根据需要选择的场次和票价分别修改config.json文件中的sess和price参数。

* 查看购票须知中实名制一栏，若无需实名制则config.json文件中的real_name参数不需要填写（即为[]）；若每笔订单只需一个证件号则real_name参数只需选择一个；若每张门票需要一个证件号，则real_name参数根据需购票数量进行相应添加。


* 若是首次登录，根据终端输出的提示，依次点击登录、扫码登录，代码将自动保存cookie文件（cookie.pkl）

* 使用前请将待抢票者的姓名、手机、地址设为默认。

* 配置完成后执行python damai_ticket.py即可,注意观察控制台输出。

* 本代码为保证抢票顺利，设置循环直到抢票成功才退出循环，若中途需要退出程序请直接终止程序。

如果你觉得我写得东西对你有所帮助，可以扫描下面的打(yao)赏(fan)二维码给我微信转账支持我，谢谢~
![在这里插入图片描述](https://img-blog.csdnimg.cn/146fa13e98214546b320f531f53b12fa.png#pic_center)

如有需求，联系方式：
![在这里插入图片描述](https://img-blog.csdnimg.cn/fcb3eec3cc3b41b5bc597c221ef71b6c.png#pic_center)


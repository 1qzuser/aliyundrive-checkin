# aliyundrive-checkin
- aliyundrive-checkin是一个定时自动签到的python程序
- 2023/5/17： 增加自动领取签到奖励、显示本月签到次数
- 2023/6/12： 增加requests出错重试，使用chatgpt优化代码结构

# 如何使用？ 
1. Fork项目到自己的仓库
2. 点击Settings -> 点击选项卡 Secrets and variables -> 点击Actions -> New repository secret



    | Name   | Secret                           |
    | ------ | ------------------------------- |
    | TOKEN *   | 阿里云盘Token 可以添加多个用英文逗号(,)分割 无需空格  |
    | SCKEY  | Server酱 推送密钥 |
    | PUSHPLUS_TOKEN  | pushplus 推送Token |
    | WECOM_WEBHOOK  | 企业微信 WEBHOOK |
    | BARK_DEVICEKEY  | IOS应用Bark 推送密钥 |

以上TOKEN为阿里云盘签到必填项 推送项选择其中一个即可 也可多渠道推送

3. 点击Actions -> 选择aliyundrive-checkin -> 点击Run workflow 运行即可

### 其它设置
- 需要调整推送内容修改aliyundrive_info.py文件即可
- 自动签到时间修改.github/workflows/checkin.yml文件 cron项即可实现
  - 该cron指定的是格林尼治时间（UTC），如果需要换算成北京时间，要在该cron的基础上增加八小时得到北京时间。

### 如何获取阿里云盘TOKEN？
- [https://alist.nn.ci/zh/guide/drivers/aliyundrive.html](https://alist.nn.ci/zh/guide/drivers/aliyundrive.html)

# 如侵权请联系本人删除

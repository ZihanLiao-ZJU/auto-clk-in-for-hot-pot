# Dimlitter-zju-dailyhealth-autocheck
<div style="text-align: center">

 ![AUR](https://img.shields.io/badge/license-MIT%20License%202.0-green.svg)
![GitHub stars](https://img.shields.io/github/stars/Dimlitter/zju-dailyhealth-autocheck.svg?style=social&label=Stars)
![GitHub forks](https://img.shields.io/github/forks/Dimlitter/zju-dailyhealth-autocheck.svg?style=social&label=Fork)

</div>

# 简介
利用github action 实现自动健康打卡

> 大家有条件的尽量把代码下载到自己仓库运行，最近github action风控较严，觉得有用的话给个star就好啦

## 写在前面
Fork自[Mrli](https://github.com/Freedomisgood)学长，我只是加了github action 执行以及推送功能

Mrli学长原库链接：https://github.com/Freedomisgood/When_Coding_in_ZJU/tree/main/Health_Checkin

`交流群组`：https://t.me/zjuers 


## 需要的secrets`必填`
```
account:通行证账号
 
password:通行证密码

lng:所打卡位置的经度 

lat:所打卡位置的纬度
```
## 可选参数`推送相关`
 ```
 
TG_TOKEN: tg bot的token 通过私聊 @botfather 获得

CHAT_ID：你账号的ID 可以通过私聊 @userinfobot 获取

DD_BOT_TOKEN: 钉钉自定义机器人的webhook后面的内容，只需 https://oapi.dingtalk.com/robot/send?access_token=XXX 等于=符号后面的XXX即可

DD_BOT_SECRET (可选)：钉钉机器人的加签密钥，如果不选择，则需在第一项添加自定义关键词"健康打卡"或其他关键词

REMINDERS : 钉钉机器人需要@的用户

```
<details> <summary> <font size=5>更新日志</font></summary>

2022.5.7 针对平台验证码，加入验证码识别功能<br>
2022.4.6 增加获取验证键值，更新`campus`参数<br>
2022.3.30 更新data包，将UA替换成钉钉内置浏览器UA<br>
2022.3.28 重新排版readme以及重构代码<br>
2022.1.15 更新data包，根据个人情况需要修改，请在check.py的172行后根据注释自行修改<br>
2021.12.24 加入钉钉机器人推送<br>
2021.12.22 更新统一认证平台登录<br>
2021.12.05 更新打卡参数<br>
2021.11.27 打卡界面发生变化 无需更新仍可使用<br>
~~2021.10.28 pysocks问题无法解决，创建dev分支<br>~~
~~2021.10.27 添加socks5代理功能，使用国内ip，增加打卡隐蔽性<br>~~
感谢 [LittleYe233](https://github.com/LittleYe233) 的大力支持<br>
2021.10.24 tg推送模块分离<br>
感谢 [zxc2012](https://github.com/zxc2012) 增加的平台登录检查功能<br>
2021.10.23 添加secrets检查提醒 增加tg bot推送判断 

</details>

## TO DO
 - [ ] 增加socks5代理功能，以解决github action服务器访问国内网站不稳定的问题
 - [ ] 实现多样化推送渠道
 - [x] 模拟真实打卡UA/随机UA

## 声明

本项目为Python学习交流的开源非营利项目，仅作为程序员之间相互学习交流之用。

使用者请遵从相关政策。对一切非法使用所产生的后果，我们概不负责。

本项目对您如有困扰请联系我们删除。
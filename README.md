# notify
使用工作流，给自己设置提醒。
结构为：
.github/
└── workflows/
    ├── remind-every-150-days.yml
    ├── renew-domain-a-yearly.yml
    └── renew-domain-b-yearly.yml

每个配置文件为一个提醒，第一个是150天，自己的一张手机卡保号提醒，第二个是一个域名续费提醒，第三个也是。第一个每150天提醒，不能使用cron,调用每天提醒，脚本内判断150天。提醒使用bark,get方法发送到手机。创建环境变量REMINDER_150DAYS_URL。url填写进去。另外两个也是同理。也可以设置成电报的机器人通知url。或者其他的通知方法，看个人喜好了。

# 说明
- 用于 OpenWRT/LEDE 路由器上进行 Server酱 微信推送的插件
- 基于 serverchan 提供的接口发送信息，Server酱说明：http://sc.ftqq.com/1.version
- 已经自带 luci

#### 主要功能
- 路由 ip 变动推送
- 设备别名
- 设备上下线推送
- CPU 负载、温度监视
- 定时推送设备运行状态
- MAC 白名单、黑名单、仅检测某接口设备
- 免打扰时间

#### 已知BUG

- 多拨环境下无法获取 wan ip，详情查看https://github.com/tty228/luci-app-serverchan/issues/8
- 由于不同设备温度文件不一样，如遇到设备温度无法正常读取，请修改
“cut -c1-2 /sys/class/thermal/thermal_zone0/temp” @KFERMercer 

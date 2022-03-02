# vips
#！这是一个根据vip(虚拟ip-keepalived)区分主从，在主上启动xxx服务的脚本，在从上停止服务
#当vip发生变更时，服务也根据vip一起发生变更！结合crontab一起使用，脚本执行频率越高，障害发生时间越短！
#脚本执行频率问题：可以结合crontab的sleep一起使用
#例如：
#!   * * * * * /bin/bash vip.sh >> /tmp/vip.log 2>&1
#!   * * * * * sleep 10; /bin/bash vip.sh >> /tmp/vip.log 2>&1
#!   * * * * * sleep 20; /bin/bash vip.sh >> /tmp/vip.log 2>&1
#!   * * * * * sleep 30; /bin/bash vip.sh >> /tmp/vip.log 2>&1
#!   * * * * * sleep 40; /bin/bash vip.sh >> /tmp/vip.log 2>&1
#!   * * * * * sleep 50; /bin/bash vip.sh >> /tmp/vip.log 2>&1

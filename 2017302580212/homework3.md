1.telnet whu.edu.cn 25
配置telnet环境。
telnet whu.edu.cn 25
EHLO hello
AUTH login
base64格式的账号
base64格式的密码
MAIL FROM：<2017302580212@whu.edu.cn>
RCPT TO:<1042957000@qq.com>
DATA
heyheyhey
.
quit

2.telnet maths.whu.edu.cn 80
telnet maths.whu.edu.cn 80
GET / HTTP/1.1 
回车 
Host：maths.whu.edu.cn
回车 回车
（注意：一定要有host且输入要快。）

课后习题：
P1.
a. 错
b. 对
c. 错
d. 错
e. 错

p7.
得到IP地址的时间 = RTT1 + RTT2 + … + RTTn
三次握手加上最后的响应 = 2 RTT0
因此总共是 2 RTT0 + RTT1 + RTT2 + … + RTTn

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

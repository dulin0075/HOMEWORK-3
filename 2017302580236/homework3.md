### *P4*

a. `http://gaia.cs.umass.edu/cs453/index.html`

b. `HTTP1.1`

c. 浏览器请求的是一条持续连接，由 `Connection: keep-alive` 看出

d. 无法看出主机的IP地址

e. 浏览器类型是`Mozilla/5.0`，服务器需要将对象的不同版本发到对应的浏览器

### *P9*

a. 在链路或速率R上传输大小为L的对象的时间是L/R，平均时间是对象的平均大小除以R：

$\delta$= (850,000 bits)/(15,000,000 bits/sec) = .0567 sec

链路上的流量强度由$\beta \delta$=(16个请求/秒)(0.567秒/请求)=0.907表示。因此，平均访问延迟为(0.567秒)/(1-0.907)≈0.6秒。因此，总的平均响应时间为0.6秒+3秒=3.6秒。

b. 由于60%的请求在机构网络中得到满足，接入链路上的业务强度降低了60%。因此，平均访问延迟为(.0567秒)/[1-(4)(.907)]=.089秒。如果请求由缓存满足(发生概率为6)，则响应时间大约为零；如果缓存丢失，平均响应时间为0.089秒，3秒=3.089秒(40%的时间)。因此，平均响应时间为(6)(0秒)(4)(3.089秒)=1.24秒。因此，平均响应时间从3.6秒缩短到1.24秒。

### *telnet1*

telnet whu.edu.cn 25

ehlo lyj736

auth login

//input base64_username `MjAxNzMwMjU4MDIzNkB3aHUuZWR1LmNu`

//input base64_passcode 

mail from:`<2017302580236@whu.edu.cn>`
rcpt to:`<3064998151@qq.com>`

data

mail from:`<2017302580236@whu.edu.cn>`
rcpt to:`<3064998151@qq.com>`
subject: hello

.

quit

![](D:\picture\分布式\telnet1.png)

### *telnet2*

telnet maths.whu.edu.cn 80

GET /kxyj/xsjz/31.htm HTTP/1.1 

Host: maths.whu.edu.cn

//摁两次回车键

![](D:\picture\分布式\math.png)

​																                                 ***2017302580236   刘一婧***
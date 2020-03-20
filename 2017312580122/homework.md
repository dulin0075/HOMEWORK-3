# HomeWork3

## P4

考虑当浏览器发送一个HTTP GET报文时，通过Wireshark俘获到下列ASCII字符串（即这是一个 HTTP GET报文的实际内容）。字符＜ cr＞ ＜lf ＞是回车和换行符（即下面文本中的斜体字符串＜ cr〉 表示了单个回车符，该回车符包含在HTTP首部中的相应位置）。回答下列问题，指出你在下面HT TP GET报文中找到答案的地方。

> GET /cs453/index.html HTTP/1.1<cr><lf>Host: gaia.cs.umass.edu<cr><lf>User-Agent: Mozilla/5.0 (Windows;U; Windows NT 5.1; en-US; rv:1.7.2) Gecko/20040804 Netscape/7.2 (ax) <cr><lr>Accept ext/xml, application/xml, application/xhtml+xml, text/html;q=0.9, text/plain;q=0.8,image/png,*/*; q=0.5 <cr><lf>Accept-Language en-us, en;q=0.5<cr><lf>Accept-Encoding zip,deflate <cr><lr>Accept-Charset ISO-8859-1,utf-8;q=0.7 r*;q=0.7<cr><lf>Keep-Alive 300<cr><lf>Connection keep-alive<cr><Jf><cr><If>

a. 由浏览器请求的文档的URL是什么？
/cs453/index.html
b. 该浏览器运行的是HTTP的何种版本？
HTTP/1.1
c. 该浏览器请求的是一条非持续连接还是一条持续连接？
由报文中最后的字段“Connection keep-alive"可知，这条连接是持续的。
d. 该浏览器所运行的主机的IP地址是什么？
无从得知
e. 发起该报文的浏览器的类型是什么？在一个HTTP请求报文中，为什么需要浏览器类型？
Mozilla/5.0。
服务器可以有效地为不同类型的用户代理实际发送相同对象的不同版本。

## P9

考虑图2-12,其中有一个机构的网络和因特网相连。假定对象的平均长度为850000比特，从这个机构网的浏览器到初始服务器的平均请求率是每秒16个请求。还假定从接入链路的因特网一侧的路由器转发一个HTTP请求开始，到接收到其响应的平均时间是3秒（参见2.2.5节）。将总的平均响应时间建模为平均接人时延（即从因特网路由器到机构路由器的时延）和平均因特网时延之和。对于平均接入时延，使用△/（1-△β)，式中△是跨越接入链路发送一个对象的平均时间，β是对象对该接入链路的平均到达率。

a. 求出总的平均响应时间。
已知:
平均因特网时延为3s；
接入链路为15Mbps；
对象的平均长度=850000b，约等于0.85Mb；
平局请求率为16个请求/s；
对象对该接入链路的平均到达率β = 1。
可算出：
△ = 0.85Mb / 15Mbps;
平均接入时延 = △ /（1-△β) = (0.85Mb / 15Mbps) / (1 - (0.85Mb / 15Mbps) * 1) = 0.06s
故总的平均响应时间 = 平均接人时延 + 平均因特网时延 = 3.06s

b. 现在假定在这个机构LAN中安装了一个缓存器。假定命中率为0.4,求出总的响应时间。
由题意知，β = 1 - 0.4 = 0.6，而其他部分与a)一致；
故总的平均响应时间 = 命中率 * 平均接人时延 + β * (平均因特网时延 + 平均接人时延)
= 0.4 * 0.06 + 0.6 * 3.06 = 1.86s

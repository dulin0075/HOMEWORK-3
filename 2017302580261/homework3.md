# 一.telnet whu.edu.cn 25

##### 1、相关指令

```
telnet whu.edu.cn 25

ehlo 1

auth login

MjAxNzMwMjU4MDI2MUB3aHUuZWR1LmNu

d20yODUwNTgy

MAIL FROM: <2017302580261@whu.edu.cn>

RCPT TO:  <313793439@qq.com>

data

测试测试测试
.
```



##### 2、结果

![捕获](C:\Users\lenovo\Desktop\捕获.PNG)

收到邮件

![捕获2](C:\Users\lenovo\Desktop\捕获2.PNG)

# 二、telnet maths.whu.edu.cn 80

```
GET / HTTP/1.1
Host: maths.whu.edu.cn
```

结果![捕获3](C:\Users\lenovo\Desktop\捕获3.PNG)

# 三、课后练习

##### 4.考虑当浏览器发送一个HTTP GET报文时，通过Wireshark俘获到下列ASCII字符串（即这是一个 HTTP GET报文的实际内容）。字符＜ cr＞ ＜lf ＞是回车和换行符（即下面文本中的斜体字符串＜ cr〉 表示了单个回车符，该回车符包含在HTTP首部中的相应位置）。回答下列问题，指出你在下面HT TP GET报文中找到答案的地方。GET /cs453/index ・html HTTP/1・1<or〉<2f>Host: gai a•cs ・ umass ・ edu<cr><2r>User-Agent: Mozilla/5 ・ 0 ( Windows;U; Windows NT 5.1; en-US; rv:1•7•2) Gee ko/20040804 Netscape/7 ・ 2 (ax) <cr><lr>Accept:ex t/xml, application/xmlz application/xhtml+xml, text /html;q=0 ・ 9, text/plain;q=0•8,image/png,*/*;q=0 ・ 5 <cr><2f>Accept-Language: en-usf en;q=0 ・ 5<cr><lf>Accept- Encoding: zip,deflatevor〉v』f〉Accept-Charset: ISO -8859-1,utf-8;q=0•7 r*;q=0 ・ 7<cr><2f>Keep-Alive: 300<cr> <1 f>Connection:keep-alive<cr><Jf><cr><If>&由浏览器请求的文档的URL是什么？ b. 该浏览器运行的是HTTP的何种版本？ c. 该浏览器请求的是一条非持续连接还是一条持续连接？ d. 该浏览器所运行的主机的IP地址是什么？ e. 发起该报文的浏览器的类型是什么？在一个HTTP请求报文中，为什么需要浏览器类型？

a  http://gaia.cs.umass.edu/cs453/index.html

b  HTTP1.1

c  持续连接

d  无法得知

e  Mozilla/5.0 根据不同类型浏览器返回不同的结果以适配浏览器

##### 5.下面文本中显示的是来自服务器的回答，以响应上述问题中HTTP GET报文。回答下列问题，指出 你在下面报文中找到答案的地方。 HTTP/1.1 200 OK<cr><ir>Date: Tue, 07 Mar 2008 12:39:4 5GMT<cr><Jf>Server: Apache/2•0 ・ 52 (Fedora) <cr><2f>Last-Modified: Satz 10 Dec2005 18:27:46 GMT<cr><lf>ETag : "526c3-f22-a88a4c80,z<cr><lf>kccept- Ranges: bytes<cr><lf>Content-Length: 3874<cr><2f> Keep-Alive: timeout=max=100<cr><ir>Connection: Keep-Alive<cr><2f>Content-Type: text/html; charset= ISO-8859-1 <cr><2f><crxlf>< ! doctype html public 〃一 //w3c//dtd html 4 ・ 0trmnsitional//en〃><c2f〉<html><lf> <heaci><2f> <meta http-equiv=z,Content-Type" conte"text/html; charset=iso-8859-lz,xIf> <meta name=〃GENERATOR〃 content=,zMozilla/4 ・ 79 [en] (Windows NT 5・0; U) Netscape] f,Xlf> <title>CMPSCI 453 / 591 / NTU-ST550ASpring 2005 homepage</titl.e><«Zf〉</head><_Zf> <much more document text following here (not shown) > -a.服务器能否成功地找到那个文档？该文档提供回答是什么时间？ b. 该文档最后修改是什么时间？ c. 文档中被返回的字节有多少？ d. 文档被返回的前5个字节是什么？该服务器同意一条持续连接吗？

a.200OK所以能够，2008年3月7日12：39：45GMT

b 2005年12月10日18：27：46GMT

c 3874

d <！ 同意
## 作业3

#### 2017312580002-周梓浩

------

### 1.telnet whu.edu.cn 25

因為帳號被鎖的關係,改用了QQ邮箱來实現

輸入如下指令:

- telnet smtp.qq.com 25

- helo localhost

- 輸入auth login

- 輸入用base64加密後的帳戶

- 輸入用base64加密後的授权碼

- 輸入

  ```
  mail from:<1085723174@qq.com>
  rcpt to:<junoworprime@outlook.com>
  data
  from:<1085723174@qq.com>
  to:<junoworprime@outlook.com>
  subject: hello
  test
  .
  ```

要注意的是需要授权碼的邮箱要用base64加密后的授权碼作為密碼登錄

![1](https://github.com/20192021855-DCAN/HOMEWORK-3/blob/master/2017312580002/1.jpg?raw=true)

![2](https://github.com/20192021855-DCAN/HOMEWORK-3/blob/master/2017312580002/2.png?raw=true)
------

## 2.telnet maths.whu.edu.cn 80

輸入如下指令:

- telnet maths.whu.edu.cn 80

- ```
  GET /index.htm HTTP/1.1
  Host: maths.whu.edu.cn
  ```

![3](https://github.com/20192021855-DCAN/HOMEWORK-3/blob/master/2017312580002/3.png?raw=true)

------

## P7

IP地址的时间 = RTT1 + RTT2 + … + RTTn

因為三次握手之后還需要有最后的响应 = 2 RTT0

 所以結果是 2 RTT0 + RTT1 + RTT2 + … + RTTn

## P10

并行非持续HTTP的T1 
T1= 3*(200b/150bps) + 100000b/150bps + 3*(200b/(150bps/10)) + 100000b/(150bps/10) = 7377.3s 
持续HTTP的T2 
T2 = 3*(200b/150bps) + 100000b/150bps + 10*(200b/150bps + 100000b/150bps) = 7351s

雖然看上去只差20多秒,但在計算机20多秒已經是很大的增益


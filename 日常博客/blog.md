### URL是什么？？
 - 统一资源的定位符
 - 用于定位于互联网上的资源

### 常用的一些协议有哪些
- http：超文本传输协议。你随便打开一个网址就看到的就是http了。

- https：一个加密的http 就等于你上了一个需要输入密码的网站

- ftp：FXP说简单点就是一个FTP客户端控制两个FTP服务器，在两个FTP服务器之间传送文件。

- file：本地协议。
- //：与当前页面协议保持一致。

 ### 把网址输入到浏览器 发生了啥事情呢？
 1. 例如你输入了https://www.baidu.com/
 2. 浏览器实际上不知道www.baidu.com是什么东西
 3. 然后浏览器就会去查找www.baidu.com这个域名的IP地址。
 4.  域名就是baidu.com
 5. （发明域名就是能语义化，好记一点）

### IP地址是什么？
- 每个处于互联中的设备都有IP地址
- 分为局域网IP 和 公网IP
- 127.0.0.1就代表本机的IP

 ### 域名解析流程
 1. 先查看浏览器缓存       先看你有没有浏览过这个网址
 2. 然后看系统缓存          从Hosts文件查找有没有这个域名
 3. 上面都没有 就查看 路由系缓存   
 4. 再没有 就查看电信 ISP DNS

 5. 好吧 都没有我只能通过域名来找相应的IP


### 服务器的处理
- 服务器是一台安装系统的机器，常见的系统如linux，weindows server2012
- 而且系统里安装了处理请求的应用 叫Web server
1.常见的web服务器有 Apache，Nginx，lls，Lighttpd
2.web服务器接收用户的Request交给网站代码，或者请求反响代理到其他web服务器。

网站处理流程
![528560fb56581ae59a16e48309835003_r.jpg](http://upload-images.jianshu.io/upload_images/8126350-8a3121bbaaa159ba.jpg?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)
ps：这里找了一下网上的图，好理解


 ##### 最后到浏览器的处理了
 1. HTML字符串被浏览器结束后被一句句读取解析
 2. 解析到link 标签后重新发送请求获取CSS
 3. 解析道script标签后发送请求获取JS，并执行代码
 ps：解析到什么就获取什么，执行什么！！！

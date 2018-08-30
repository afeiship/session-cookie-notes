# set-cookie AND cookie:
> 如果你把Cookies看成为http协议的一个扩展的话，理解起来就容易的多了，其实本质上cookies就是http的一个扩展。


## cookie && set-cookie:
~~~
有两个http头部是专门负责设置以及发送cookie的,它们分别是Set-Cookie以及Cookie。
当服务器返回给客户端一个http响应信息时，其中如果包含Set-Cookie这个头部时，
1. 意思就是指示客户端建立一个cookie
2. 并且在后续的http请求中自动发送这个cookie到服务器端，直到这个cookie过期。
3. 如果cookie的生存时间是整个会话期间的话，那么浏览器会将cookie保存在内存中，浏览器关闭时就会自动清除这个cookie。
4. 另外一种情况就是保存在客户端的硬盘中，浏览器关闭的话，该cookie也不会被清除，下次打开浏览器访问对应网站时，这个cookie就会自动再次发送到服务器端。
~~~

## Cookie 的设置过程：
> 一个cookie的设置以及发送过程分为以下四步：

1. 客户端发送一个http请求到服务器端 
2. 服务器端发送一个http响应到客户端，其中包含Set-Cookie头部 
3. 客户端发送一个http请求到服务器端，其中包含Cookie头部 
4. 服务器端发送一个http响应到客户端

![设置过程如下](https://images.cnblogs.com/cnblogs_com/andy-zhou/811282/o_Cookie_Session001.png)

~~~
在客户端的第二次请求中包含的Cookie头部中，提供给了服务器端可以用来唯一标识客户端身份的信息。
这时，服务器端也就可以判断客户端是否启用了cookies。
尽管，用户可能在和应用程序交互的过程中突然禁用cookies的使用，但是，这个情况基本是不太可能发生的，所以可以不加以考虑，这在实践中也被证明是对的。
~~~
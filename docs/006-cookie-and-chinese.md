# Unicode编码：保存中文

~~~
中文与英文字符不同，中文属于Unicode字符，在内存中占4个字符，而英文属于ASCII字符，内存中只占2个字节。
Cookie中使用Unicode字符时需要对Unicode字符进行编码，否则会乱码。

提示：Cookie中保存中文只能编码。
一般使用UTF-8编码即可。
不推荐使用GBK等中文编码，因为浏览器不一定支持，而且JavaScript也不支持GBK编码。
~~~

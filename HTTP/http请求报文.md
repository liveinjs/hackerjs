HTTP报文是面向文本的，报文中的每一个字段都是一些ASCII码串，各个字段的长度是不确定的。HTTP有两类报文：请求报文和响应报文。

HTTP请求报文

一个HTTP请求报文由请求行（request line）、请求头部（header）、空行和请求数据4个部分组成，下图给出了请求报文的一般格式。

![abc](https://raw.github.com/hackerjs/hackerjs/master/HTTP/images/2012072810301161.png)

or

＜request-line＞

＜headers＞

＜blank line＞

[＜request-body＞]

回车换行符: /r/n

# HybridNSURLProtocol
一个基于WKWebView的hybirde的容器。能拦截所有WKWKWebView的的css,js,png等网络请求的demo
NSURLProtocol 子类，就可以对 app 内所有的网络请求进行:

```
[NSURLProtocol registerClass:[HybridNSURLProtocol class]];

```


可是在 WKWebView 中的请求却完全不遵从这一规则，只是象征性+ (BOOL) canInitWithRequest:(NSURLRequest *)request 方法，之后的整个请求流程似乎就与 NSURLProtocol 完全无关了。

使我WKWebView 的一度认为请求不遵守NSURLProtocol协议，所以不走 NSURLProtocol。这个也是很苦扰我的问题。导致我们hybird的容器1.0也是是用UIWebVIew实现的。



![Aaron Swartz](https://github.com/LiuShuoyu/HybirdWKWebVIew/blob/master/jpeg/WechatIMG1.jpeg)



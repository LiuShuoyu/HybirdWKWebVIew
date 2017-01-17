# WKWebView OC/Swift版 一款IOS8以后的web加载神器
WKWebView 支持POST请求 加载本地页面 直接加载网页 JS交互 集成支付宝/微信URL支付功能  仿微信返回按钮
```
允许访问HTTP链接
HTTPS权限:
<key>NSAppTransportSecurity</key>
<dict>
<key>NSAllowsArbitraryLoads</key>
<true/>
</dict>


/**
 加载纯外部链接网页

 @param string URL地址
 */
- (void)loadWebURLSring:(NSString *)string;
/**
 加载本地网页
 
 @param string 本地HTML文件名
 */
- (void)loadWebHTMLSring:(NSString *)string;

/**
 加载外部链接POST请求(注意检查 WKJSPOST.html 文件是否存在 )
 postData请求块 注意格式：@"\"username\":\"xxxx\",\"password\":\"xxxx\""
 
 @param string 需要POST的URL地址
 @param postData post请求块
 */
- (void)POSTWebURLSring:(NSString *)string postData:(NSString *)postData;


Swift版本

///加载普通URL
let webView = WKWebViewController()
webView.loadUrlSting(string: "https://www.baidu.com")

/// 加载本地HTML
/// 直接传入文件名即可
let webView = WKWebViewController()
webView.loadUrlSting(string: fileName)

/// POST方式请求加载
/// postString: post参数体 详情请搜索swift/oc转义字符（注意格式："\"username\":\"aaa\",\"password\":\"123\""）
let webView = WKWebViewController()
webView.loadUrlSting(string: url, postString: postString)


```

![Aaron Swartz](https://github.com/LiuShuoyu/HybirdWKWebVIew/blob/master/jpeg/WechatIMG1.jpeg)



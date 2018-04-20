# Cookie

## 会话期 Cookie
   - 新创建的 Cookie 默认为会话期 Cookie，浏览器关闭就自动失效（有些浏览器有会话自动恢复功能）

## 持久性 Cookie
   - 可以指定一个特定的过期时间 setMaxAge 设定最长存活时间，单位为秒
   
## Cookie 作用域
   - Domain 和 Path 定义了 Cookie 的作用域，表示 Cookie 可以发送给哪些 URL
   - 默认的 Domain 为当前 URL 对应的 hostname(不包含子域名)  setDomain
   - 默认的 Path 为当前 URL 对应的 path，  setPath
   
## Cookie 的 Secure 和 HttpOnly 标记
   - Secure 标记表示该 Cookie 只能由 HTTPS 发送
   - HttpOnly 表示该 Cookie 无法在客户端被 Javascript 读取到。一般该 Cookie 都绑定服务端的 Session 信息

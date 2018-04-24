# Cookie
1. 服务器端通过 response header 字段来让浏览器保存 Cookie，如： Set-Cookie: username=JinJie
1. 浏览器通过 request header 字段来向服务器发送 Cookie，如：Cookie: username=JinJie

## 会话期 Cookie
   - 新创建的 Cookie 默认为会话期 Cookie，浏览器关闭就自动失效（有些浏览器有会话自动恢复功能）

## 持久性 Cookie
   - 可以指定一个特定的过期时间 setMaxAge 设定最长存活时间，单位为秒 `setMaxAge(100)`   
   
在 servlet 里如何删除客户端里的 cookie？
   
## Cookie 作用域
   - Domain 和 Path 定义了 Cookie 的作用域，表示 Cookie 可以发送给哪些 URL
   - 默认的 Domain 为当前 URL 对应的 hostname(不包含子域名) `setDomain("jsj.tzc.edu.cn")`
   - 默认的 Path 为当前 URL 对应的 path，`setPath("/message_board")`
   
## Cookie 的 Secure 和 HttpOnly 标记
   - Secure 标记表示该 Cookie 只能由 HTTPS 发送
   - HttpOnly 表示该 Cookie 无法在客户端被 Javascript 读取到。一般该 Cookie 都绑定服务端的 Session 信息

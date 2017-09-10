## $\_SERVER

是一个包含了诸如头信息\(header\)、路径\(path\)、以及脚本位置\(script locations\)等等信息的数组。这个数组中的项目由 Web 服务器创建。不能保证每个服务器都提供全部项目

```
PHP_SELF：当前文件的文件名 __FILE__ 常量包含当前(例如包含)文件的完整路径和文件名
```

```
QUERY_STRING：查询的字符串

REQUEST_METHOD：请求方法

SCRIPT_FILENAME：当前脚本的绝对路径

HTTP_ACCEPT_LANGUAGE：浏览器语言

HTTP_ACCEPT_ENCODING：浏览器支持的能够接受的编码类型

HTTP_ACCEPT：浏览器接受的类型列表

HTTP_USER_AGENT：检查浏览页面的访问者在用什么操作系统

HTTP_UPGRADE_INSECURE_REQUESTS：是否过渡https

HTTP_CONNECTION：keep-alive HTTP的链接方式，持久方式
```




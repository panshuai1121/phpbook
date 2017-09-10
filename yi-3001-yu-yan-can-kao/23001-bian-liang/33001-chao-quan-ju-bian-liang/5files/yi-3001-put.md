## PUT

简单地说：通常用于向服务器发送请求，如果URI不存在，则要求服务器根据请求创建资源，如果存在，服务器就接受请求内容，并修改URI资源的原始版本。 必须使用标准的输入流来读取一个 HTTP PUT 的内容

```
<?php
/* PUT data comes in on the stdin stream */
$putdata = fopen("php://stdin", "r");

/* Open a file for writing */
$fp = fopen("myputfile.ext", "w");

/* Read the data 1 KB at a time
   and write to the file */
while ($data = fread($putdata, 1024))
  fwrite($fp, $data);

/* Close the streams */
fclose($fp);
fclose($putdata);
?>
```

```
PUT /path/filename.html HTTP/1.1
```

这通常意味着远程客户端会将其中的/path/filename.html存储到 web 目录树。让 Apache 或者 PHP 自动允许所有人覆盖 web 目录树下的任何文件显然是很不明智的。因此，要处理类似的请求，必须先告诉 web 服务器需要用特定的 PHP 脚本来处理该请求。在 Apache 下，可以用_Script_选项来设置。它可以被放置到 Apache 配置文件中几乎所有的位置。通常我们把它放置在 &lt;Directory&gt; 区域或者 &lt;Virtualhost&gt; 区域。可以用如下一行来完成该设置：

```
Script PUT /put.php

```

这将告诉 Apache 将所有对 URI 的 PUT 请求全部发送到 put.php 脚本，这些 URI 必须和 PUT 命令中的内容相匹配

  



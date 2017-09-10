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




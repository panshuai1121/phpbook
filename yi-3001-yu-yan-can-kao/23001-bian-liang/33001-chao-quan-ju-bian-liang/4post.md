## $\_POST

当 HTTP POST 请求的 Content-Type 是_application/x-www-form-urlencoded_或_multipart/form-data_时，会将变量以关联数组形式传入当前脚本。



```
<?php
echo 'Hello ' . htmlspecialchars($_POST["name"]) . '!';
?>
```




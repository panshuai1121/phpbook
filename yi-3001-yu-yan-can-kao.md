## 语言参考

### 1、PHP标记

符合PSR-1 规则，PHP代码文件 **必须 **以&lt;?php 或 &lt;?= 标签开始，如果是纯PHP代码，最好删除PHP结束标记

另外PHP段标签的模式 可以在php.ini 中** short\_**_**open\_tag** 配置_

```
<?php

echo "Hello Wrold";
```

### 2、指令分隔符

PHP 需要在每个语句后用分号结束指令。一段 PHP 代码中的结束标记隐含表示了一个分号；在一个 PHP 代码段中的最后一行可以不用分号结束。如果后面还有新行，则代码段的结束标记包含了行结束。

```
<?php
    echo "This is a test";
?>

<?php echo "This is a test" ?>

<?php echo 'We omitted the last closing tag';
```

### 3、注释

```
/*
 这是一个多行的注释
*/
echo "Hello Wrold"; //我是一个单行的
#我也是一个单行的注释
```




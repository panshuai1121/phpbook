# array\_combine

array\_combine 创建一个数组，用一个数组的值作为其键名，另一个数组的值作为其值

```
array array_combine ( array $keys , array $values )
```

参数：

keys： 作为新数组的键，非法的值将会转换成字符串

values：作为array的值

返回：

合并后的数组，如果两个数组单元数不匹配会有警告

```
$aArr = ["shuai","chao","she","he"];
$bArr = ["28","28","28"];

$cArr = array_combine($aArr,$bArr);

print_r($cArr);

Warning: array_combine(): Both parameters should have an equal number of elements in /usr/local/nginx/html/php7Learn/index.php on line 8
```




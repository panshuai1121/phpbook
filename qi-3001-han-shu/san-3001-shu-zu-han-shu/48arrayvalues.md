# array\_values

返回数组中的值

```
array array_values ( array $array )
```

参数 ：

array：需要返回值的数组

返回值：

返回所有值的索引数组

```
<?php
$a = array(
3 => 11,
1 => 22,
2 => 33,
);
$a[0] = 44;

print_r( array_values( $a ));
==>
Array(
  [0] => 11
  [1] => 22
  [2] => 33
  [3] => 44
)
?>
```




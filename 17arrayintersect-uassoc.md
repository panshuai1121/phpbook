# array\_intersect\_uassoc

带索引检查计算数组的交集，用回调函数比较索引

```
array array_intersect_uassoc ( array $array1 , array $array2 [, array $... ], callable $key_compare_func )
```

参数：

array ：用来比较的数组

callable: 用户自定义的处理函数

返回值：

在第一个参数小于，等于或大于第二个参数时，该比较函数必须相应地返回一个小于，等于或大于 0 的整数。

```
int callback ( mixed $a, mixed $b )
```

```
<?php
$array1 = array("a" => "green", "b" => "brown", "c" => "blue", "red");
$array2 = array("a" => "GREEN", "B" => "brown", "yellow", "red");

print_r(array_intersect_uassoc($array1, $array2, "strcasecmp"));
```

结果：

```
Array
(
    [b] => brown
)
```




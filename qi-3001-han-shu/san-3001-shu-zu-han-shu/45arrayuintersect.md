# array\_uintersect

array\_uintersect—计算数组的交集，用回调函数比较数据

```
array array_uintersect ( array $array1 , array $array2 [, array $... ], callable $value_compare_func )
```

array\_uintersect\(\) 返回一个数组，该数组包含了所有在 array1 中也同时出现在所有其它参数数组中的值。数据比较是用回调函数进行的。 此比较是通过用户提供的回调函数来进行的。如果认为第一个参数小于，等于，或大于第二个参数时必须分别返回一个小于零，等于零，或大于零的整数。

参数：

array1：第一个数组。

array2：第二个数组。

value\_compare\_func：在第一个参数小于，等于或大于第二个参数时，该比较函数必须相应地返回一个小于，等于或大于 0 的整数。

```
int callback ( mixed $a, mixed $b )
```

```
<?php
$array1 = array("a" => "green", "b" => "brown", "c" => "blue", "red");
$array2 = array("a" => "GREEN", "B" => "brown", "yellow", "red");

print_r(array_uintersect($array1, $array2, "strcasecmp"));
?>
```




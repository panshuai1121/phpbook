# array\_intersect\_assoc

带索引检查计算数组的交集

```
array array_intersect_assoc ( array $array1 , array $array2 [, array $... ] )
```

参数：

array ：操作的数组

返回值：

返回数组，该数组包含了所有在array1中也同时出现在所有其它参数数组中的值。

```
$arr = array("a"=>1, "b"=>2, "c"=>3, "d"=>4, "e"=>5);

$arr1 = array("b"=>1, "a"=>2,"c"=>3);

print_r(array_intersect_assoc($arr,$arr1));

#结果

Array ( [c] => 3 )
```




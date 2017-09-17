# array\_intersect\_key

使用键名比较计算数组的交集

```
array array_intersect_key ( array $array1 , array $array2 [, array $... ] )
```

array\_intersect\_key\(\) 返回一个数组，该数组包含了所有出现在 array1 中并同时出现在所有其它参数数组中的键名的值

参数：

array：需要比较的数组

返回值：

返回一个数组，该数组包括了所有出现在`array1`中并且出现在任何其它参数数组中的键名的值

```
$arr = array("a"=>1, "b"=>2, "c"=>3, "d"=>4, "e"=>5);

$arr1 = array("b"=>1, "a"=>2,"c"=>3);

print_r(array_intersect_key($arr,$arr1));
```

结果：

```
Array ( [a] => 1 [b] => 2 [c] => 3 )
```




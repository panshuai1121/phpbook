# array\__fill\_keys_

使用指定的键和值填充数组

```
array array_fill_keys ( array $keys , mixed $value )
```

参数：

keys：使用该数组的值作为键

values：填充的值

返回：

填充后的数组

```
$arr1 = ["id"];
$arr2  = 123;
print_r(array_fill_keys($arr1,$arr2));
#结果
Array ( [id] => 123 )
```




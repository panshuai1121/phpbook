# array\_uintersect\_assoc

带索引检查计算数组的交集，用回调函数比较数据

```
array array_uintersect_assoc ( array $array1 , array $array2 [, array $... ], callable $value_compare_func )
```

参数

array1

第一个数组。

array2

第二个数组。

value\_compare\_func

在第一个参数小于，等于或大于第二个参数时，该比较函数必须相应地返回一个小于，等于或大于 0 的整数。

```
int callback ( mixed $a, mixed $b )
```






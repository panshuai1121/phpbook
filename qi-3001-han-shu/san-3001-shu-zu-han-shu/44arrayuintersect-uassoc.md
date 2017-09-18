# array\_uintersect\_uassoc

带索引检查计算数组的交集，用单独的回调函数比较数据和索引

```
array array_uintersect_uassoc ( array $array1 , array $array2 [, array $... ], callable $value_compare_func , callable $key_compare_func )
```

通过额外的索引检查、回调函数比较数据和索引来返回多个数组的交集。

参数：

```
array1
第一个数组。

array2
第二个数组。

value_compare_func
在第一个参数小于，等于或大于第二个参数时，该比较函数必须相应地返回一个小于，等于或大于 0 的整数。

int callback ( mixed $a, mixed $b )
key_compare_func
键名比较的回调函数。
```




# array\_diff\_ukey

用回调函数对键名比较计算数组的差集

```
array array_diff_ukey ( array $array1 , array $array2 [, array $... ], callable $key_compare_func )
```

参数：

array：需要比较的数组

callable key ：用户自定义的回调函数

```
在第一个参数小于，等于或大于第二个参数时，该比较函数必须相应地返回一个小于，等于或大于 0 的整数。

int callback ( mixed $a, mixed $b )
```




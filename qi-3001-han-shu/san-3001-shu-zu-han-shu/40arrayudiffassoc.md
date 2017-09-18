# array\_udiff\_assoc

array\_udiff\_assoc—带索引检查计算数组的差集，用回调函数比较数据

```
array array_udiff_assoc ( array $array1 , array $array2 [, array $... ], callable $value_compare_func )
```

此比较是通过用户提供的回调函数来进行的。如果认为第一个参数小于，等于，或大于第二个参数时必须分别返回一个小于零，等于零，或大于零的整数。

参数 :

array1

第一个数组。

array2

第二个数组。

value\_compare\_func

在第一个参数小于，等于或大于第二个参数时，该比较函数必须相应地返回一个小于，等于或大于 0 的整数。

```
int callback ( mixed $a, mixed $b )
```




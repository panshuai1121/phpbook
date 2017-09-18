# array\_uintersect

array\_uintersect—计算数组的交集，用回调函数比较数据

```
array array_uintersect ( array $array1 , array $array2 [, array $... ], callable $value_compare_func )
```

array\_uintersect\(\) 返回一个数组，该数组包含了所有在 array1 中也同时出现在所有其它参数数组中的值。数据比较是用回调函数进行的。 此比较是通过用户提供的回调函数来进行的。如果认为第一个参数小于，等于，或大于第二个参数时必须分别返回一个小于零，等于零，或大于零的整数。




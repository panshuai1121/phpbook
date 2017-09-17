# array\_map

为数组每个元素应用回调函数

```
array array_map ( callable $callback , array $array1 [, array $... ] )
```

参数：

callable：处理数组每一个元素的回调函数

array：需要处理的数组

返回值：

回数组，包含 callback 函数处理之后 array1 的所有元素。

**注意：**

**需要处理多个数组时，callback函数的参数，必须与处理数组列表的数量相同**




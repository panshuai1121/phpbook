# array\_filter

用回调函数过滤数组中的单元

```
array array_filter ( array $array [, callable $callback [, int $flag = 0 ]] )
```

依次将 array 数组中的每个值传递到 callback 函数。如果 callback 函数返回 true，则 array 数组的当前值会被包含在返回的结果数组中。数组的键名保留不变。

参数：

array ：使用的数组

callable：使用回调函数，如果没有回调函数 会将数组中 **值等价为false的值删除**

flag：

**`ARRAY_FILTER_USE_KEY`**-`callback`接受键名作为的唯一参数

**`ARRAY_FILTER_USE_BOTH`**-`callback`同时接受键名和键值




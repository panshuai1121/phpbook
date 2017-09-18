# array\_unique

移出数组中重复的值

```
array array_unique ( array $array [, int $sort_flags = SORT_STRING ] )
```

注意键名保留不变。**array\_unique\(\)**先将值作为字符串排序，然后对每个值只保留第一个遇到的键名，接着忽略所有后面的键名。这并不意味着在未排序的`array`中同一个值的第一个出现的键名会被保留

参数：

array 输入的数组。

sort\_flags 第二个可选参数sort\_flags 可用于修改排序行为：

排序类型标记：

SORT\_REGULAR - 按照通常方法比较（不修改类型）

SORT\_NUMERIC - 按照数字形式比较

SORT\_STRING - 按照字符串形式比较

SORT\_LOCALE\_STRING - 根据当前的本地化设置，按照字符串比较。


# array\_unique

移出数组中重复的值

```
array array_unique ( array $array [, int $sort_flags = SORT_STRING ] )
```

注意键名保留不变。**array\_unique\(\)**先将值作为字符串排序，然后对每个值只保留第一个遇到的键名，接着忽略所有后面的键名。这并不意味着在未排序的`array`中同一个值的第一个出现的键名会被保留




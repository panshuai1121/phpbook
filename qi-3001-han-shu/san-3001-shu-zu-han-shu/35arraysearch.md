# array\_search

在数组中搜索给定的值，如果成功则返回首个相应的键名

```
mixed array_search ( mixed $needle , array $haystack [, bool $strict = false ]
```

 参数：

needle ：需要查找的值

如果`needle`是字符串，则比较以区分大小写的方式进行。

haystack：查找的数组

strict：

如果可选的第三个参数 strict 为 TRUE，则 array\_search\(\) 将在 haystack 中检查完全相同的元素。 这意味着同样严格比较 haystack 里 needle 的 类型，并且对象需是同一个实例






# array\_pad

以指定长度将一个值填充进数组

```
array array_pad ( array $array , int $size , mixed $value )
```

array\_pad\(\) 返回 array 的一个拷贝，并用 value 将其填补到 size 指定的长度。如果 size 为正，则填补到数组的右侧，如果为负则从左侧开始填补。如果 size 的绝对值小于或等于 array 数组的长度则没有任何填补。有可能一次**最多填补 1048576 个单元**。




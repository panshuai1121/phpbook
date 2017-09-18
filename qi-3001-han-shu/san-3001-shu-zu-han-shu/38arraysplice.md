# array\_splice

去掉数组中的某一部分并用其它值取代

```
array array_splice ( array &$input , int $offset [, int $length = count($input) [, mixed $replacement = array() ]] )
```

把 input 数组中由 offset 和 length 指定的单元去掉，如果提供了 replacement 参数，则用其中的单元取代。

**注意 input 中的数字键名不被保留**。




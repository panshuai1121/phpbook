# array\_column

取出数组中指定的列

语法：

```
array array_column ( array $input , mixed $column_key [, mixed $index_key = null ] )
```

参数：

input ：需要取出列的多维数组，如果提供的是包含一组对象的数组，只有 public 属性会被直接取出。 为了也能取出 private 和 protected 属性，类必须实现**\_\_get\(\)**和**\_\_isset\(\)**魔术方法。




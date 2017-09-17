# array\_column

取出数组中指定的列

语法：

```
array array_column ( array $input , mixed $column_key [, mixed $index_key = null ] )
```

参数：

input ：需要取出列的多维数组，如果提供的是包含一组对象的数组，只有 public 属性会被直接取出。 为了也能取出 private 和 protected 属性，类必须实现**\_\_get\(\)**和**\_\_isset\(\)**魔术方法。

column-key：需要返回的列它可以是索引数组的列索引，或者是关联数组的列的键，也可以是属性名。 也可以是`NULL`，此时将返回整个数组（配合`index_key`参数来重置数组键的时候，非常管用）

**index\_key**：作为返回数组的索引/键的列，它可以是该列的整数索引，或者字符串键值






# array\_push

将一个或多个单选压入数组的末尾（入栈）

```
int array_push ( array &$array , mixed $value1 [, mixed $... ] )
```

array\_push\(\) 将 array 当成一个栈，并将传入的变量压入 array 的末尾。array 的长度将根据入栈变量的数目增加。和如下效果相同：

```
<?php
$array[] = $var;
?>

```




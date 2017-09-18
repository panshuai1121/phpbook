# array\_sum

array\_sum 对数组中所有的值进行求和

```
number array_sum ( array $array )
```

参数：

array：输入的数组

返回值：

**array\_sum\(\)**将数组中的所有值相加，并返回结果



```
<?php
$a = array(2, 4, 6, 8);
echo "sum(a) = " . array_sum($a) . "\n";

$b = array("a" => 1.2, "b" => 2.3, "c" => 3.4);
echo "sum(b) = " . array_sum($b) . "\n";
?>
```




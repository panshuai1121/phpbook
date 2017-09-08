## 生成器

生成器允许你在 [foreach](http://php.net/manual/zh/control-structures.foreach.php) 代码块中写代码来迭代一组数据而不需要在内存中创建一个数组, 那会使你的内存达到上限，或者会占据可观的处理时间。相反，你可以写一个生成器函数，就像一个普通的自定义 [函数](http://php.net/manual/zh/functions.user-defined.php)一样, 和普通函数只[返回](http://php.net/manual/zh/functions.returning-values.php)一次不同的是, 生成器可以根据需要[yield](http://php.net/manual/zh/language.generators.syntax.php#control-structures.yield)多次，以便生成需要迭代的值。

---

### 生成器的优势

迭代大型数据集或数列时最适合使用生成器，因为这样占用的系统内存最少。生成器也能完成迭代器能完成的简单任务，而且使用的代码更少。

总而言之，生成器并没有为PHP添加新功能，不过使用生成器大大简化了某些任务，而且使用的内存更少，如果需要更多功能，例如在数据集中执行后退、快进以及查找功能，最好自己编写实现Iterator接口的类，或者使用PHP标准库（SPL）中某个原生的迭代器。



```
<?php

function makeRange($length) {
   $dataSet = [];
   for ($i = 0; $i < $length ;$i++ ) {
     $dataSet[] = $i;
   }
   return $dataSet;
}

$customRange = makeRange(10000000);

foreach ($customRange as $i) {
   echo $i.PHP_EOL;
}
#结果会报错
#PHP Fatal error:  Allowed memory size of 134217728 bytes exhausted (tried to allocate 134217736 bytes) in makeRange.php on line 6
#Fatal error: Allowed memory size of 134217728 bytes exhausted (tried to allocate 134217736 bytes) in makeRange.php on line 6

```




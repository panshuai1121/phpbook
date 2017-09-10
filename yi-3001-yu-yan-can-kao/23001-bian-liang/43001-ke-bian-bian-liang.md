## 可变变量

一个可变变量获取了一个普通变量的值作为这个可变变量的变量名

要将可变变量用于数组，必须解决一个模棱两可的问题。这就是当写下

$$a\[1\]时，解析器需要知道是想要 $a\[1\] 作为一个变量呢，还是想要 $$a 作为一个变量并取出该变量中索引为 \[1\] 的值。解决此问题的语法是，对第一种情况用 ${$a\[1\]} ，对第二种情况用 ${$a}\[1\]

```
<?php
class foo {
    var $bar = 'I am bar.';
    var $arr = array('I am A.', 'I am B.', 'I am C.');
    var $r   = 'I am r.';
}

$foo = new foo();
$bar = 'bar';
$baz = array('foo', 'bar', 'baz', 'quux');
echo $foo->$bar . "\n";
echo $foo->$baz[1] . "\n";

$start = 'b';
$end   = 'ar';
echo $foo->{$start . $end} . "\n";

$arr = 'arr';
echo $foo->$arr[1] . "\n";
echo $foo->{$arr}[1] . "\n";

?>
```




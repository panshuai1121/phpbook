## Abstract 、Final、Static

需要添加 abstract final static 的，abstract、final **必须 **放在修饰符前 ，static **必须 **放在其后。

```
<?php
namespace Vendor\Package;

abstract class ClassName
{
    protected static $foo;
    abstract protected function zim();
    final public static function bar()
    {

    }  
}
```

### 1 方法及函数调用

方法及函数调用时，方法名或函数名与参数左括号之间**一定不可**有空格，参数右括号前也**一定不可**有空格。每个参数前**一定不可**有空格，但其后**必须**有一个空格。

```
<?php
bar();
$foo->bar($arg1);
Foo::bar($arg2, $arg3);
```

参数**可以**分列成多行，此时包括第一个参数在内的每个参数都**必须**单独成行。

```
<?php
$foo->bar(
    $longArgument,
    $longerArgument,
    $muchLongerArgument
);
```




## 类、属性和方法

此处的「类」泛指所有的「class类」、「接口」以及「traits 可复用代码块」。

### 1、扩展与继承

关键词 extends 和 implements **必须** 写在同一行；

类的开始花括号 **必须 **独占一行，结束花括号也 **必须 **在类主体后独占一行；

`implements`的继承列表也 **可以 **分成多行，这样的话，每个继承接口名称都 **必须 **分开独立成行，包括第一个；

```
<?php
namespace Vender\Package;

use FooClass;
use BarClass as Bar;
use OtherVender\OderPackage\BazClass;

Class Foo extends FooClass implements \ArrayAccess, \Countable
{

}

#也可以
Class Foo extends FooClass implements
    \ArrayAccess,
    \Countable
{

}
```

## 2、属性

* 每个属性 **必须 **添加修饰访问符；
* **一定不可以 **使用关键字 var 声明一个属性；
* 一条语句 **不可** 声明多个属性；
* **不该 **使用下划线作为前缀，来区分属性是 protected 或 private。

```
<?php
namespace Vendor\Package;

class ClassName
{
    public $foo = null;
}
```

## 3、方法

* 所有的方法 必须 添加修饰符；
* 方法名称后 **一定不可 **有空格符，其开始花括号 **必须 **独占一行，结束花括号也 **必须 **在方法主体后单独成一行。参数左括号后和右括号前 **一定不可 **有空格；
* **不该 **使用下划线作为前缀，来区分方法是 protected 或 private。

```
<?php
namespace Vender\Package;

Class ClassName
{
    public function fooBarBaz($arg1, $arg2, $arg3 = [])
    {
        //method body
    }  
}
```

#### 3.1 方法参数

参数列表中，每个参数逗号后边 **必须 **有一个空格，而 逗号前边**一定不可**有空格；




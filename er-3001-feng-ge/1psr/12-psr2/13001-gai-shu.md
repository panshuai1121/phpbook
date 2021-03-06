## 概述

代码 **必须** 遵循 PSR-1的编码规范。

代码 **必须 **使用4个空格缩进 而不是TAB键 进行缩进。

每行的字符数应该保持在80个之内，理论上 **一定不可 多于120个，但 一定不可 有硬性限制。**

每个 namespace 命名空间声明语句和 use 声明语句块后面，**必须** 插入一个空白行。

类（class）的开始的花括号 { **必须** 放在其声明后独自一行，右 花括号 } 则 **必须 **放到 类 主体下边自成一行。

方法的开始花括号 {** 必须 **写在函数声明之后 独自一行，右 花括号 } 也 **必须** 在函数主体后 自成一行。

类的属性和方法 **必须 **添加修饰符（public、private、protected ），abstract、final **必须** 声明在修饰符之前，而 static **必须 **声明在修饰方法之后。

控制结构的关键字 必须 要有一个空格符，而调用方法或函数时则 **一定不可 **有。

控制结构的开始 花括号 { 必须 写在声明的同一行，而结束花括号 } **必须 **写在主体后自成一行。

控制体结构开始的左括号后和结束右括号前，都 **一定不可 **有空格符。

例子：

```
namespace Vendor\Package;

use FooInterFace;
use BarClass as Bar;
use OrderVender\OtherPackage\BazClass;

class Foo extends Bar implements FooInterFace
{
    public function sampleFunction($a,$b = null)
    {
        if ($a === $b) {
            bar();
        } else if ($a > $b) {
            $foo->bar($arg1);
        } else {
            BazClass::bar($arg2,$arg3);
        }
    }

    final public static function bar()
    {
      
    }
}
```




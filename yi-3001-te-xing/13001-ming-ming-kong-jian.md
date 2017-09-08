## 命名空间

5.3.0中开始引入，作用是按照一种虚拟的层次结构组织PHP代码，这种层次结构类似操作系统中文件系统的目录结构。

**PHP组件和框架都放在各自全局唯一的厂商命名空间，以免与其他得厂商使用的常见类名冲突。**

声明命名空间的代码始终放在&lt;?php 标签后的第一行。

**大多数PHP组件为了兼容广泛使用的PSR-4自动加载标准，会把子命名空间放到文件系统的子目录中**

```
<?php

namespace Symfony\Component\HttpFoundation;
```

---

### 别名

应该在PHP文件的顶部使用use关键字导入代码，放在&lt;?php命名空间声明之后，使用use关键字前不用加 会默认为w安全限定命名空间。

use 关键字必须出现在全局作用域（不能在函数类中），因为是在编译时使用。

**首先要注意的是命名空间只起申明作用，也就是在使用了命名空间的时候依然得把这个命名空间申明的那个文件包含进来。在使用中可以通过 `__NAMESPACE__`来查看当前命名空间**

    <?php 
    namespace B;
    use A;

    const test = 'Btest';
    function test() { 
        return __FUNCTION__; 
    }

    class Test{
        public function __construct(){
            return __METHOD__;
        }
    }

    include "a.php";//必须包含A命名空间的文件

    // 完全限定
    // `\B\test`从绝对位置查找输出，如果是全局函数则`\test`
    echo \B\test;   //输出Btest

    // 限定名称  
    // 这里已经通过`use A`申明了在这个文件可以通过`\A\...`使用A命名空间的函数
    echo A\test;    //输出Atest

    // 非限定名称
    // 非限定名称的函数`test`会从当前命名控件查找，即B
    echo test;      //输出Btest

    // namespace关键字代表当前命名空间
    echo namespace\test;
    ?>




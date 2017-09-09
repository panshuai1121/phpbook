## 超全局变量

**超全局变量是在全部作用域中始终可用的内置变量，**PHP 中的许多预定义变量都是“超全局的”，这意味着它们在一个脚本的全部作用域中都可用。在函数或方法中无需执行 **global $variable **就可以访问它们。

超全局变量：

$GLOBALS;

$\_POST;

$\_GET;

$\_REQUEST;

$\_ENV;

$\_FILES;

$\_SERVER;

$\_SESSION;

$\_COOKIE;


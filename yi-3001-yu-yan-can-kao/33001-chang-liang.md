## 常量

常量是一个简单值的标识符（名字）。如同其名称所暗示的，在脚本执行期间该值不能改变，常量默认为大小写敏感。传统上常量标识符总是大写的

常量名和其它任何 PHP 标签遵循同样的命名规则。合法的常量名以字母或下划线开始，后面跟着任何字母，数字或下划线。用正则表达式是这样表达的：

_\[a-zA-Z\_\x7f-\xff\]\[a-zA-Z0-9\_\x7f-\xff\]\*\_

可以用define 和 const 关键字来定义常量，一个常量一旦被定义，就不能再改变或者取消定义，可以用[constant\(\)](http://php.net/manual/zh/function.constant.php) 来获取常量的值

**Note**:

和使用[define\(\)](http://php.net/manual/zh/function.define.php)来定义常量相反的是，使用_const_关键字定义常量必须处于最顶端的作用区域，因为用此方法是在编译时定义的。这就意味着不能在函数内，循环内以及_if_语句之内用_const_来定义常量。

### 常量和变量有如下不同：

* 常量前面没有美元符号 _$_；
* 常量只能用 [define\(\)](http://php.net/manual/zh/function.define.php) 函数定义，而不能通过赋值语句；
* 常量可以不用理会变量的作用域而在任何地方定义和访问；
* 常量一旦定义就不能被重新定义或者取消定义；
* 常量的值只能是标量。

### const 与 define的不同

**\(1\).const用于类成员变量的定义，一经定义，不可修改。define不可用于类成员变量的定义，可用于全局常量。  
\(2\).const可在类中使用，define不能。  
\(3\).const不能在条件语句中定义常量。**  
例如：  
if \(...\){  
const FOO = 'BAR'; // 无效的invalid  
}  
if \(...\) {  
define\('FOO', 'BAR'\); // 有效的valid  
}  
**\(4\).const采用一个普通的常量名称，define可以采用表达式作为名称。**  
const FOO = 'BAR';  
for \($i = 0; $i &lt; 32; ++$i\) {  
define\('BIT\_' . $i, 1 &lt;&lt; $i\);  
}  
**\(5\).const只能接受静态的标量，而define可以采用任何表达式。**  
例如：  
const BIT\_5 = 1 &lt;&lt; 5; // 无效的invalid  
define\('BIT\_5', 1 &lt;&lt; 5\); // 有效的valid  
**\(6\).const定义的常量时大小写敏感的，而define可通过第三个参数（为true表示大小写不敏感）来指定大小写是否敏感。**  
例如：  
define\('FOO', 'BAR', true\);  
echo FOO; // BAR  
echo foo; // BAR


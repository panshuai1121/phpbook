## $\_GET

$\_GET 用于通过url 传递过来的变量数组，Superglobal”也称为自动化的全局变量。这就表示其在脚本的所有作用域中都是可用的。不需要在函数或方法中用 **global $variable; **来访问它

```
echo 'Hello'.$_GET['a'];
```

### magic\_quotes\_gpc

当 magic\_quotes 为 on，所有的 ' \(单引号\)、" \(双引号\)、\（反斜杠）和 NUL's 被一个反斜杠自动转义。






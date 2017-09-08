## **内置HTTP服务器**

不要再生产环境中使用，在测试环境中使用还是很好的。无需安装WAMP .MAMP 或大型web服务器，就能本地预览HTML；

```
PHP -S localhost:4000
```

---

**配置服务器**

如果团队人员需要共享，可以把配置文件放在版本控制中。

```
PHP -S localhost:8000 -C app/config/php.ini
```

**路由配置**

```
PHP -S localhost：8000 -c router.php
```




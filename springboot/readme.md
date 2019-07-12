pom.xml
```
<!-- 导入配置文件 -->
<properties resource="**.properties"/>

之后的属性可以使用 **.prepertie 定义的变量 如：
"${spring.datasource.driver-class-name}"
```

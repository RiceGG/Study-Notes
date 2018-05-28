##注解
@RequestParam(required = true,defaultValue="234") String id;
required = true <br>
传参必须有值，否则报错<br>

@ResponseBody<br>
设置响应数据为json<br>

@RequestBody
在springmvc方法参数上添加 标注后的参数接收json数据<br>



#thymeleaf模版工具
thymeleaf模版可以完美的实现jsp的功能，而且后缀名为.html,方便前后端分离。<br>

##引入依赖
&lt;dependency><br>
      &lt;groupId>org.springframework.boot&lt;/groupId> <br>
      &lt;artifactId>spring-boot-starter-thymeleaf&lt;/artifactId><br>
&lt;/dependency><br>

##该工具如何避免过严的语法检查
[来源](https://www.jianshu.com/p/b361a6acbe0c)<br>
###1.首先在application.properties中修改spring.thymeleaf.mode属性：
spring.thymeleaf.mode=LEGACYHTML5
###2.引入依赖
&lt;dependency><br>
    &lt;groupId>net.sourceforge.nekohtml&lt;/groupId><br>
    &lt;artifactId>nekohtml&lt;/artifactId><br>
    &lt;version>1.9.21&lt;/version><br>
&lt;/dependency>
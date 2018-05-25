## cmd项目根目录
mvn -Pnexus spring-boot:run<br>

运行spring-boot项目<br>

mvn -Pnexus package<br>

将sprint-boot项目打包<br>

mvn spring-boot:run -Dlogging.level.root=warn -Drun.arguments="--name=Daniel"<br>

关闭log信息并运行项目		后面--name是修改propereits的name属性<br>

java -jar target\bt--SNAPSHOT.jar<br>

运行jar包<br>

## 在application.properties中修改端口号
server.port=9999<br>

## 启用spring-boot项目需要在main方法中使用

SpringApplication.run(当前类.class,args);<br>

## CommandLineRunner和ApplicationRunner
这两个是spring-boot的两个接口，都可以在web容器启动是执行。<br>

比如：数据库连接，删除临时文件，清除缓存信息<br>

不同点：ApplicationRunner中run方法的参数为ApplicationArguments，而CommandLineRunner接口中run方法的参数为String数组。<br>

学习来源：[csdn-【从零开始学Spring Boot】](https://blog.csdn.net/gebitan505/article/details/55047819)
<br>

##spring boot的junit




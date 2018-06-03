##注解
@RequestParam(required = true,defaultValue="234") String id;
required = true <br>
传参必须有值，否则报错<br>

@ResponseBody<br>
设置响应数据为json<br>

@RequestBody
在springmvc方法参数上添加 标注后的参数接收json数据<br>

@validate
在参数上后台验证
BingResult 接收验证错误的消息

#thymeleaf模版工具
thymeleaf模版可以完美的实现jsp的功能，而且后缀名为.html,方便前后端分离。<br>

<a th:href="@{'/update?id='+${prod.id}}"></a>
##关闭缓存
spring.thymeleaf.cache=false
##引入依赖
&lt;dependency><br>
      &lt;groupId>org.springframework.boot&lt;/groupId> <br>
      &lt;artifactId>spring-boot-starter-thymeleaf&lt;/artifactId><br>
&lt;/dependency><br>

##该工具如何避免过严的语法检查
[来源](https://www.jianshu.com/p/b361a6acbe0c)<br>
在使用前需要注意要使用nekoHTML版本1.9.15以上才可以
###1.首先在application.properties中修改spring.thymeleaf.mode属性：
spring.thymeleaf.mode=LEGACYHTML5
###2.引入依赖
&lt;dependency><br>
    &lt;groupId>net.sourceforge.nekohtml&lt;/groupId><br>
    &lt;artifactId>nekohtml&lt;/artifactId><br>
    &lt;version>1.9.21&lt;/version><br>
&lt;/dependency>

restful接口

只接受和发送json数据


##swagger 

自动生成文档

@Configuration
@EnableSwagger2
配置swagger的配置文件
public class Swagger2Configuration {
	public Docket buildDocket() {
		return new Docket(DocumentationType.SWAGGER_2)
				.apiInfo(buildApiInf())
				.select()
				.apis(RequestHandlerSelectors.basePackage("com.example.web"))
				.paths(PathSelectors.any())
				.build();
	}
	
	private ApiInfo buildApiInf() {
		return new ApiInfoBuilder()
				.title("我的项目")
				.description("请仔细查看")
				.termsOfServiceUrl("localhost:8080")
				.contact(new Contact("guyu", "localhost:8080", "aa@bb.c"))
				.build();
	}
}

@ApiOperation
标注在方法上
@Api(value="dashboard",tags= {"控制器功能"})
标注在控制器上

查询文档网址swagger-ui.html
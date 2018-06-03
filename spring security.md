[太极开发者社区](http://tech.taiji.com.cn/)
<br>内部有关于安全规范标准
## security配置方式 ##
    @EnableWebSecurity
	//配置web安全配置
    public class WebSecurityConfig extends WebSecurityConfigurerAdapter {
	@Bean
	public UserDetailsService userDetailsService() throws Exception {
		//在内存中（配置文件中）加载用户的账户信息
		InMemoryUserDetailsManager manager = new InMemoryUserDetailsManager();
		//添加用户名密码和角色
		manager.createUser(User.withUsername("user").password("password").roles("USER").build());
		return manager;
	}
	}

[源码讲解](http://aasonwu.iteye.com/blog/2055625)
<br>源码中加载了好多安全和权限设置<br>

	//当不使用spring或springmvc是推荐以这种方式加载配置文件
	public class SecurityWebApplicationInitializer
		extends AbstractSecurityWebApplicationInitializer {
		public SecurityWebApplicationInitializer() {
			super(WebSecurityConfig.class);
		}
	}


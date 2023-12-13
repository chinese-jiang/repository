# application.properties配置



#驱动类名称

```properties
spring.datasource.driver-class-name=com.mysql.cj.jdbc.Driver
```

#数据库连接的url

```properties
spring.datasource.url=jdbc:mysql://localhost:3306/tlias
```

#连接数据库的用户名

```properties
spring.datasource.username=root
```

#连接数据库的密码

```properties
spring.datasource.password=1234
```

#配置mybatis的日志, 指定输出到控制台

```properties
mybatis.configuration.log-impl=org.apache.ibatis.logging.stdout.StdOutImpl
```

#开启mybatis的驼峰命名自动映射开关 a_column ------> aCloumn

```properties
mybatis.configuration.map-underscore-to-camel-case=true
```


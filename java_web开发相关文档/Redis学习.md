# Redis

## 一、简介

Redis是一个基于内存的key-value数据库

1. 启用

   ```
   redis-server.exe redis.windows.conf
   ```

2. 连接redis服务（使用redis）

   ```
   redis-cli.exe -h localhost（连接的主机） -p 6379(端口号) -a 758014(密码)
   ```


## 二、 spring Data Redis: java使用redis框架

1. 导入maven坐标

   ```xml
   <dependency>
       <groupId>org.springframework.boot</groupId>
       <artifactId>spring-boot-starter-data-redis</artifactId>
   </dependency>
   ```

2. 配置Redis数据源

   ```yml
   # yml
   spring:
     redis:
       host: ${sky.redis.host}
       port: ${sky.redis.port}
       database: ${redis.redis.database}
   # dev.yml下
   sky:
     redis:
       host: localhost
       port: 6379
       #    password: 758014
       #    有16个库DB0-DB15，指定使用DB1数据库
       database: 1
   ```

3. 编写配置类，创建RedisTemplate对象

   ```java
   @Configuration
   @Slf4j
   public class RedisConfiguration {
   
   
       @Bean
       public RedisTemplate redisTemplate(RedisConnectionFactory redisConnectionFactory){
           log.info("开始创建redis对象");
           RedisTemplate redisTemplate = new RedisTemplate();
           // 设置redis连接工厂对象
           redisTemplate.setConnectionFactory(redisConnectionFactory);
           // 设置key序列化器
           redisTemplate.setKeySerializer(new StringRedisSerializer());
           // 设置value序列化器
           redisTemplate.setValueSerializer(new StringRedisSerializer());
           return redisTemplate;
       }
   }
   
   ```

   

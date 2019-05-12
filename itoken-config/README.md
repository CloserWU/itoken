每个`config`客户端
 - `pom.xml`加入这个依赖

    ```xml
    <dependency>
       <groupId>org.springframework.cloud</groupId>
       <artifactId>spring-cloud-config-client</artifactId>
    </dependency>
    ```

 - 在`application.yml`文件中，
    ```yml
    spring:
      cloud:
        config:
          label: master
          name: itoken-zuul
          uri: http://locahost:8888
          profile: dev
    ```

 - 在`mainClass`类下加上注解`@EnableDiscoveryClient`

即可生效`config`客户端
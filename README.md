## Springboot3.0以上集成Swagger2
1.	新建一个springboot项目，记得一定要选择Maven和右边添加Spring Web dependency
https://start.spring.io/
 
2.	导入springboot starter包到IDE。
   
3.	如果8080端口有冲突的话，可在src -> main -> resources -> application.properties里单独规定新端口，如添加一行：
```application.properties
server.port = 8091 //8091是我人为规定的新端口
```

4.	pom.xml添加依赖dependency。3.0以上springboot切勿使用springfox和springfox UI，否则会有null pointer或者 TypeNotPresentException.
```pom.xml
  <dependency>
     <groupId>org.springdoc</groupId>
     <artifactId>springdoc-openapi-starter-webmvc-ui</artifactId>
     <version>2.3.0</version>
  </dependency>
```

5.	新建config包，创建SwaggerConfig类
The Swagger UI page will then be available at (http://localhost:8091/swagger-ui/index.html)
Ref: https://stackoverflow.com/questions/71549614/springfox-type-javax-servlet-http-httpservletrequest-not-present




Spring is developed by Pivotal.
Framework with built-in bindings for web, REST API, micro-services, Relational & nosql DB, Security.
www.spring.io
## Spring Technology Stack:
1.  Support for SQL and NOSQL: JDBC, MongoDB, Elastic Search, Redis
2.  Spring Cloud: Load balancer, api gateway, production monitoring tool,m messaging system (RabbitMQ, Kafka).

Spring Boot Application -> Web application (Request, Response, GET, POST, JSP, JSTL, Bootstrap), MVC (Model, View, Validation, Form Tags, Dispatch Servlet, 
View Resolver), Spring Boot(Starters, Auto Configuration).

Starting a Sample Web Application:
Spring intiaalizer : Initialize Spring boot application. (spring.io)

Spring Framework : Core support for dependency injection, transaction management, web applicaitons, data access, messaging, testing and more.

Spring makes it easy to create Java enterprise applicaitons. 

Spring favors interface/class separation.
-> Wirte code in terms of interfaces.
-> Tell Spring which classes to provide implementation of the interfaces. Spring will automatically "wire" everything together.
i.e. write code in terms of interfaces and spring will use classes at runtime to plugin those interfaces.

Dependency injection -> major benefit of Spring.

Autowiring: Inject the object dependency implicitly. It internally uses setter or constructor injection. It works only with references not with primitives such
as - string or int values.
Autowiring means "autowire by type" first. This works if there is exactly one bean of that type (class) available.

@ComponentScan: It is used with the @Configuration annotation and tells Spring, the packages to scan for annotated compnents.

@Component : Java class declared with @Component is found during the classpath scanning and registered in the context as a Spring bean. @Service, @Repository, 
@Controller are varieties  of @Component used in specific use cases.

@Qualifier: Avoids confusion when autorwiring bean more than one bean of the same type.

Spring Boot has embedded web server.
spring-boot-starter-web : for developing web applications and restful services.
spring-boot-devtools: features for developing productive applications
spring-boot-starter-test: unit and integration tests.

Whay is happening in the backgroud of request ? (Browser request)
Browser sends Http Request to Web Server
Code in Web Server => Input:HttpRequest, Output: HttpResponse
Web Server responds with Http Response

Spring boot starter web brings in some in built dependencies like -
spring mvc, spring core, Data binding (jackson bingding), validation (hibernate-validator), embedded tomcat server
Spring Boot: starter dependency provides auto configuration. Where there is Spring MVC dependency needed, spring boot directly configures DispatcherServlet.





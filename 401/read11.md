# Spring

## Read 11

### Joshua McCluskey

### Serving Web Content with Spring MVC

- Springs uses a controller for HTTP request
- Find the controller: `@Controller`
- `@GetMapping` ensures HTTP GET requests
- `@RequestParam` query string parameter
- Use spring-boot-devtools which allows live refreshes
- `@SpringBootApplication` adds configurations to run app
- `./gradlew bootRun` you can run app via gradle

### Spring MVC and Thymeleaf: how to access data from templates

- Model Attributes: Spring MVC pieces of data accessed during views
- Model Attributes are also called 
- `addAttributes`
- `ModelAndView`

```HTML
<tr th:each="message : ${messages}">
            <td th:text="${message.id}">1</td>
            <td><a href="#" th:text="${message.title}">Title ...</a></td>
            <td th:text="${message.text}">Text ...</td>
        </tr>
```
[credit: Thymeleaf](https://www.thymeleaf.org/doc/articles/springmvcaccessdata.html)

- `session` session prefix to `setAttributes`
- `#servletContext` prefix for attributes shared between requests and sessions
- `@beanName` prefix for accessing beans


### Readings
[Serving Web Content with Spring MVC](https://spring.io/guides/gs/serving-web-content/)

[Spring MVC and Thymeleaf: how to access data from templates](https://www.thymeleaf.org/doc/articles/springmvcaccessdata.html)

[<=== Back](../README.md)
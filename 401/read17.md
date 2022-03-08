# Spring Authorization

## Read 17

### Joshua McCluskey

### Spring Boot and OAuth2

- Using social login
- Either Googele or GitHub
- OAuth2.0 and Spring Boot
- Run main in SocialApplication
  
### Single Sign On with GitHub

- Add homepage by creating an index.html
- Add in Jquery and Twitter Bootstrap

````Java
<dependency>
	<groupId>org.webjars</groupId>
	<artifactId>jquery</artifactId>
	<version>3.4.1</version>
</dependency>
<dependency>
	<groupId>org.webjars</groupId>
	<artifactId>bootstrap</artifactId>
	<version>4.3.1</version>
</dependency>
<dependency>
	<groupId>org.webjars</groupId>
	<artifactId>webjars-locator-core</artifactId>
</dependency>

<dependency>
	<groupId>org.springframework.boot</groupId>
	<artifactId>spring-boot-starter-oauth2-client</artifactId>
</dependency>
````
[Credit](https://spring.io/guides/tutorials/spring-boot-oauth2/)

- GitHub acts as a resource server that verifys your info and sends out a token

- You'll  change the client side with JQuery

````Java
@SpringBootApplication
@RestController
public class SocialApplication extends WebSecurityConfigurerAdapter {

    // ...

    @Override
    protected void configure(HttpSecurity http) throws Exception {
    	// @formatter:off
        http
            .authorizeRequests(a -> a
                .antMatchers("/", "/error", "/webjars/**").permitAll()
                .anyRequest().authenticated()
            )
            .exceptionHandling(e -> e
                .authenticationEntryPoint(new HttpStatusEntryPoint(HttpStatus.UNAUTHORIZED))
            )
            .oauth2Login();
        // @formatter:on
    }

}
````

[Credit](https://spring.io/guides/tutorials/spring-boot-oauth2/)

````Java
<dependency>
    <groupId>org.webjars</groupId>
    <artifactId>js-cookie</artifactId>
    <version>2.1.0</version>
</dependency>
````

[Credit](https://spring.io/guides/tutorials/spring-boot-oauth2/)

````Java
$.ajaxSetup({
  beforeSend : function(xhr, settings) {
    if (settings.type == 'POST' || settings.type == 'PUT'
        || settings.type == 'DELETE') {
      if (!(/^http:.*/.test(settings.url) || /^https:.*/
        .test(settings.url))) {
        // Only send the token to relative URLs i.e. locally.
        xhr.setRequestHeader("X-XSRF-TOKEN",
          Cookies.get('XSRF-TOKEN'));
      }
    }
  }
});
````

[Credit](https://spring.io/guides/tutorials/spring-boot-oauth2/)

- You can create a sticker page that has multipl;e accounts to choose from. Either Google or GitHub
- You can also have a local user database



#### Reading

[Spring Boot and OAuth2](https://spring.io/guides/tutorials/spring-boot-oauth2/)

[<=== Back](../README.md)**~~**

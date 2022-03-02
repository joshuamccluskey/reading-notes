# Related Resources and Integration Testing

## Read 13

### Joshua McCluskey

### Working with Relationships in Spring Data REST

#### One-to-one relationship
- `@OneToOne` use this annotation to establish One-To-One Realationship
- Make sure eveything everything they have a DIFFERENT NAME or JsonMappingException
- Extend each repository with CrudRepository
- `curl -i -X POST -H "Content-Type:application/json"
  -d '{"name":"My Library"}' http://localhost:8080/libraries
  ` syntax to create a POST
````Java
curl -i -X POST -H "Content-Type:application/json"
        -d '{"location":"Main Street nr 5"}' http://localhost:8080/addresses

        {
        "location" : "Main Street nr 5",
        "_links" : {
        "self" : {
        "href" : "http://localhost:8080/addresses/1"
        },
        "address" : {
        "href" : "http://localhost:8080/addresses/1"
        },
        "library" : {
        "href" : "http://localhost:8080/addresses/1/library"
        }
        }
        }

````
[Credit](https://www.baeldung.com/spring-data-rest-relationships)
Syntax examples for PUT GET DELETE
````Java
curl -i -X PUT -d "http://localhost:8080/addresses/1" 
  -H "Content-Type:text/uri-list" http://localhost:8080/libraries/1/libraryAddress
        
curl -i -X GET http://localhost:8080/addresses/1/library

curl -i -X DELETE http://localhost:8080/libraries/1/libraryAddress
````

[Credit](https://www.baeldung.com/spring-data-rest-relationships)


- `@ManyToOne` Use annotation for a One-to-many relationship
- `@ManyToMany` Use annotation for a many-to-many relationship

### Set up Testing Endpoints

````Java
@RunWith(SpringRunner.class)
@SpringBootTest(classes = SpringDataRestApplication.class, 
  webEnvironment = WebEnvironment.DEFINED_PORT)
public class SpringDataRelationshipsTest {

    @Autowired
    private TestRestTemplate template;

    private static String BOOK_ENDPOINT = "http://localhost:8080/books/";
    private static String AUTHOR_ENDPOINT = "http://localhost:8080/authors/";
    private static String ADDRESS_ENDPOINT = "http://localhost:8080/addresses/";
    private static String LIBRARY_ENDPOINT = "http://localhost:8080/libraries/";

    private static String LIBRARY_NAME = "My Library";
    private static String AUTHOR_NAME = "George Orwell";
}
````
[Credit](https://www.baeldung.com/spring-data-rest-relationships)

Example testing a Relationship

````Java
@Test
public void whenSaveOneToOneRelationship_thenCorrect() {
    Library library = new Library(LIBRARY_NAME);
    template.postForEntity(LIBRARY_ENDPOINT, library, Library.class);
   
    Address address = new Address("Main street, nr 1");
    template.postForEntity(ADDRESS_ENDPOINT, address, Address.class);
    
    HttpHeaders requestHeaders = new HttpHeaders();
    requestHeaders.add("Content-type", "text/uri-list");
    HttpEntity<String> httpEntity 
      = new HttpEntity<>(ADDRESS_ENDPOINT + "/1", requestHeaders);
    template.exchange(LIBRARY_ENDPOINT + "/1/libraryAddress", 
      HttpMethod.PUT, httpEntity, String.class);

    ResponseEntity<Library> libraryGetResponse 
      = template.getForEntity(ADDRESS_ENDPOINT + "/1/library", Library.class);
    assertEquals("library is incorrect", 
      libraryGetResponse.getBody().getName(), LIBRARY_NAME);
}

````
[Credit](https://www.baeldung.com/spring-data-rest-relationships)
### Integration Testing in Spring
- An extension interface that has clases that inegrate with JUnit 5

````Java
@ExtendWith(SpringExtension.class)
@ContextConfiguration(classes = { ApplicationConfig.class })
@WebAppConfiguration
public class GreetControllerIntegrationTest {
    ....
}

@ContextConfiguration(locations={""})

@WebAppConfiguration(value = "")
````
[Credit](https://www.baeldung.com/integration-testing-in-spring)


- MockMVC encapsulates app beans to use for testing

````Java
private MockMvc mockMvc;
@BeforeEach
public void setup() throws Exception {
    this.mockMvc = MockMvcBuilders.webAppContextSetup(this.webApplicationContext).build();
}
````
[Credit](https://www.baeldung.com/integration-testing-in-spring)

Verifying testing configurations

````Java
@Test
public void givenWac_whenServletContext_thenItProvidesGreetController() {
    ServletContext servletContext = webApplicationContext.getServletContext();
    
    Assert.assertNotNull(servletContext);
    Assert.assertTrue(servletContext instanceof MockServletContext);
    Assert.assertNotNull(webApplicationContext.getBean("greetController"));
}
````
[Credit](https://www.baeldung.com/integration-testing-in-spring)

- Once you have your test set up invoke your endpoints
- You will send GET requests POST requests
- Knowing it's limitations MockMVC Spring mocks the HTTP requests and might not support all the things for a Spring App

### Readings
[Working with Relationships in Spring Data REST](https://www.baeldung.com/spring-data-rest-relationships)

[Integration Testing in Spring](https://www.baeldung.com/integration-testing-in-spring)

[<=== Back]
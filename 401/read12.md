# Spring RESTful Routing & Static Files

## Read 12

### Joshua McCluskey

### CrudRepository, JpaRepository, and PagingAndSortingRepository in Spring Data

- CRUDRepository: provides CRUD
- PagingAndSortingRepository: pagination and sorting methods
- JpaRepository: Flushes presistence context and delete records 


#### Crud Repository 

````Java
public interface CrudRepository<T, ID extends Serializable>
  extends Repository<T, ID> {

    <S extends T> S save(S entity);

    T findOne(ID primaryKey);

    Iterable<T> findAll();

    Long count();

    void delete(T entity);

    boolean exists(ID primaryKey);
}
````
[Credit: Baeldung](https://www.baeldung.com/spring-data-repositories)

- Crud functions `save(); finOne(); findAll(); count(); delete(); exists();`

#### PageAndSortingRepository

````Java
public interface PagingAndSortingRepository<T, ID extends Serializable> 
  extends CrudRepository<T, ID> {

    Iterable<T> findAll(Sort sort);

    Page<T> findAll(Pageable pageable);
    
    Sort sort = new Sort(new Sort.Order(Direction.ASC, "lastName"));
    Pageable pageable = new PageRequest(0, 5, sort);
}
````
[Credit: Baeldung](https://www.baeldung.com/spring-data-repositories)

- Paging and Sorting functions: Page size; Current page number; Sorting


#### JpaRepository

````Java
public interface JpaRepository<T, ID extends Serializable> extends
  PagingAndSortingRepository<T, ID> {

    List<T> findAll();

    List<T> findAll(Sort sort);

    List<T> save(Iterable<? extends T> entities);

    void flush();

    T saveAndFlush(T entity);

    void deleteInBatch(Iterable<T> entities);
}
````
[Credit: Baeldung](https://www.baeldung.com/spring-data-repositories)

- Jpa Methods: `findAll(); save(); save(); flush(); saveAndFlush(); deleteBatch();`

### Accessing Data with JPA

- Dependencies needed Spring Data JPS and H2 Database
- Spring initializer will take care of most of what you need 
- @Entity, @Id and @Generate4Value annotations are used in the focus class
- @Bean automatically runs the code when the programs launch
- Build Jar `./gradlew build` and `java -jar build/libs/gs-accessing-data-jpa-0.1.0.jar` This should've been done in initializer

### Readings
[CrudRepository, JpaRepository, and PagingAndSortingRepository in Spring Data](https://www.baeldung.com/spring-data-repositories)

[Spring MVC and Thymeleaf: how to access data from templates](https://www.thymeleaf.org/doc/articles/springmvcaccessdata.html)

[<=== Back](../README.md)
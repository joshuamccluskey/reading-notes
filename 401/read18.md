# Web App Security

## Read 18

### Joshua McCluskey

### Many to Many 

- @many-to-many
- A many to many relationship are like project and employees
- An empoloyee can have multiple projects and a projects can have multiple employess
- To setup database you need to set up the tables for your many to many relationship
- Model calls need to have a setup similar to below

````Java
@Entity
@Table(name = "Employee")
public class Employee { 
    // ...
 
    @ManyToMany(cascade = { CascadeType.ALL })
    @JoinTable(
        name = "Employee_Project", 
        joinColumns = { @JoinColumn(name = "employee_id") }, 
        inverseJoinColumns = { @JoinColumn(name = "project_id") }
    )
    Set<Project> projects = new HashSet<>();
   
    // standard constructor/getters/setters
    @Entity
    @Table(name = "Project")
    public class Project {
        // ...  

        @ManyToMany(mappedBy = "projects")
        private Set<Employee> employees = new HashSet<>();

        // standard constructors/getters/setters   
    }

}
````
[credit](https://www.baeldung.com/hibernate-many-to-many)

- @ManyToMany
- @JoinTable - owning side 
- @JoinColumn - the inverse side of the relationship

### This World of Ours
- Create good passwords

#### Reading

[Hibernate Many to Many](https://www.baeldung.com/hibernate-many-to-many)
[This World of Ours](chrome-extension://efaidnbmnnnibpcajpcglclefindmkaj/viewer.html?pdfurl=https%3A%2F%2Fscholar.harvard.edu%2Ffiles%2Fmickens%2Ffiles%2Fthisworldofours.pdf&clen=1681871&chunk=true)

[<=== Back](../README.md)
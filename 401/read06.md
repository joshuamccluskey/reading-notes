# Inheritance and Interfaces

## Read 06

### Joshua McCluskey

#### Inheritance 

In OOP you inherit commonly used states and behaviors from classes. The Superclass
has the properties that all subclasses or child  classes inherit. This allows
the subclass to have  unique properties that other subclasses don't have.

- If subclass is in the same package as its parent then it can inherit 
private members of the parent class. 
- Java supports multiple inheritance of type which is the ability of the
- You can override an inherited method
- If a static method had the same signature in  parent class
the subclass will hide the parent class method
- Polymorphism the idea that you can have the same characteristics and unique ones
- fields myst be accessed using `super` `super();` `super(parameter list);`
- Using `final` can prevent a method from being overridden
#### Interface

Objects interact with the methods that they expose. The interface is how you 
interact with the object.

Syntax:

```Java
class myDog implements Dog {
    String bark = "Bark";
    String sit= "I am sitting";
    String layDown = "I'm down";
    String highFive = "I'm giving High Five!";
    String guard = " I'm guarding";
    
    String myDogBarks(String bark){
        return bark;
    }
    String myDogSits(String sit){
        return sit;
    }
    String myDogDown(String layDown){
        return layDown;
    }
    String myDogFive(String highFive){
        return highFive;
    }
    String myDogGuard(String guard){
        return guard;
    }
    
}
```

- Interfaces can be APIs that have methods that can be used in the interface.
- An interface can extend any number of interfaces
- Abstract method is followed by a semicolon but no braces
- Default methods use a `default` modifier
- Static methods use a `static` modifier
- static methods are implicitly public so adding public is redundant
- All constant values are implicitly `public, static, and final` which can be omitted

- Object must be instantiated to implement the interface
- If you plan on updating or changing an interface in use consider making a new interface or use `extends`
[<=== Back](../README.md)

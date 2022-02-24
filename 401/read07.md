# Inheritance and Interfaces Day 2

## Read 07

### Joshua McCluskey

#### Inheritance 


What's the difference between an abstract class and an interface, and what are the advantages or situations you would use each?
This was very similar question that I came up from my research as we move deeper into classes and inheritance. Besides the syntactical differences where the abstract class uses the keyword abstract and the  interface uses both interface and implements they both function in a similar manner by allowing subclasses to have access to the method.

In interface, you have to implement your interface method in the implementing class. I boiled it down to using an interface when you have dissimilar subclasses that you need to have access to a method and do certain thing. For example, you can pick and choose an Animal subclass to  implement the bark() method, since not all animals bark. You can implement as many interfaces as you need to while extending one class.

In abstract class, you can't instantiate a new object with, but you can make subclasses with it. With this in mind every subclass will have access to the abstract method declared in the abstract class. You have to use the abstract method, but can make the method unique to that subclass. In an abstract class, every subclass will have all the properties and abstract methods associated with that abstract class.



Sources:

[Article Abstracts vs. Interfaces](https://www.baeldung.com/java-interface-vs-abstract-class)

[Video on Abstracts and Interfaces](https://www.youtube.com/watch?v=HvPlEJ3LHgE) 

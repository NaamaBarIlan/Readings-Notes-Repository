# Object Oriented Principles

### Reading List:

##### [Inheritance](https://docs.microsoft.com/en-us/dotnet/csharp/programming-guide/classes-and-structs/inheritance)
##### [Abstract](https://docs.microsoft.com/en-us/dotnet/csharp/programming-guide/classes-and-structs/abstract-and-sealed-classes-and-class-members)
##### [Polymorphism](https://docs.microsoft.com/en-us/dotnet/csharp/programming-guide/classes-and-structs/polymorphism)
##### [OOP Principles](https://docs.microsoft.com/en-us/dotnet/csharp/programming-guide/concepts/object-oriented-programming)
##### C# in a Nutshell - Chapter 3

---

#### Object Oriented Principles

C# provides full support for object-oriented programming including abstraction, encapsulation, inheritance, and polymorphism.

* **Abstraction** means hiding the unnecessary details from type consumers.
* **Encapsulation** means that a group of related properties, methods, and other members are treated as a single unit or object.
* **Inheritance** describes the ability to create new classes based on an existing class.
* **Polymorphism** means that you can have multiple classes that can be used interchangeably, even though each class implements the same properties or methods in different ways.

#### Inheritance

* Inheritance enables you to create new classes that reuse, extend, and modify the behavior defined in other classes.
* The class whose members are inherited is called the **base class**, and the class that inherits those members is called the **derived class**.
* Inheritance is **transitive** A derived class can have only one direct base class, but if ClassC is derived from ClassB, and ClassB is derived from ClassA, ClassC inherits the members declared in ClassB and ClassA.

#### Abstract

* The purpose of an abstract class is to provide a common definition of a base class that multiple derived classes can share.
* Classes can be declared as abstract by putting the keyword `abstract` before the class definition.
* An abstract class cannot be instantiated. 
* Abstract classes may also define abstract methods. This is accomplished by adding the keyword abstract before the return type of the method.

#### Polymorphism

* Polymorphism is a Greek word that means "many-shaped" and it refers to two distinct aspects in OOP.
* At run time, objects of a derived class may be treated as objects of a base class in places such as method parameters and collections or arrays. When this polymorphism occurs, the object's declared type is no longer identical to its run-time type
* Base classes can define and implement virtual methods, and derived classes can override them, which means they provide their own definition and implementation.
* The **virtual** keyword is used to modify a method, property, indexer, or event declaration and allow for it to be overridden in a derived class. 
* In your source code you can call a method on a base class, and cause a derived class's version of the method to be executed.
* Virtual methods enable you to work with groups of related objects in a **uniform** way.

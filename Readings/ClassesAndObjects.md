# Classes & Objects

### Reading List:

##### [Classes](https://docs.microsoft.com/en-us/dotnet/csharp/programming-guide/classes-and-structs/classes)
##### [Constructors](https://docs.microsoft.com/en-us/dotnet/csharp/programming-guide/classes-and-structs/constructors)
##### [Properties](https://docs.microsoft.com/en-us/dotnet/csharp/programming-guide/classes-and-structs/properties)
##### [Stack and Heap](https://www.c-sharpcorner.com/article/C-Sharp-heaping-vs-stacking-in-net-part-i/)
##### [Garbage Collection Fundamentals](https://docs.microsoft.com/en-us/dotnet/standard/garbage-collection/fundamentals)
##### C# in a Nutshell - Chapter 3

---
### Classes

* A type that is defined as a class is a reference type. 
* At run time, when you declare a variable of a reference type, the variable contains the value null until you explicitly create an instance of the class by using the new operator, or assign it an object of a compatible type that may have been created elsewhere.
* When the object is created, enough memory is allocated on the managed heap for that specific object, and the variable holds only a reference to the location of said object. 

### Constructors

* Whenever a class or struct is created, its constructor is called. A class or struct may have multiple constructors that take different arguments. 
* A constructor is a method whose name is the same as the name of its type. 
* Its method signature includes only the method name and its parameter list; it does not include a return type. 
* If you don't provide a constructor for your class, C# creates one by default that instantiates the object and sets member variables to the default values.

### Properties

* A property is a member that provides a flexible mechanism to read, write, or compute the value of a private field. 
* Properties can be used as if they are public data members, but they are actually special methods called accessors. This enables data to be accessed easily and still helps promote the safety and flexibility of methods.

### Stack and Heap

* The Stack and the Heap are the two places the .NET framework stores items in memory as your code executes.
* The Stack is responsible for keeping track of what is executing in our code, what has been "called".  
* The Heap is responsible for keeping track of our objects (mostly data).

### Garbage Collection 

* In the common language runtime (CLR), the garbage collector (GC) serves as an automatic memory manager. 
* The garbage collector manages the allocation and release of memory for an application. 
* For developers working with managed code, this means that you don't have to write code to perform memory management tasks. 
* Automatic memory management can eliminate common problems, such as forgetting to free an object and causing a memory leak or attempting to access memory for an object that's already been freed.
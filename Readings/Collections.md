# Collections & Enums

### Reading List:

##### [Collections](https://docs.microsoft.com/en-us/dotnet/csharp/programming-guide/concepts/collections)
##### [Enums](https://docs.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/enum)
##### C# .0 In a Nutshell - Ch. 7 Collections
##### C# 7.0 in a Nutshell: Pg 118-124

---

#### Collections

* Collections provide a more flexible way than arrays to working with groups of objects. 
* Unlike arrays, the group of objects you work with can grow and shrink dynamically as the needs of the application change. 
* For some collections, you can assign a key to any object that you put into the collection so that you can quickly retrieve the object by using the key.
* A collection is a class, so you must declare an instance of the class before you can add elements to that collection.
* If a collection contains elements of only one data type, you can use one of the classes in the System.Collections.Generic namespace.

##### Common Collection Classes:

* System.Collections.Generic classes
  * A generic collection is useful when every item in the collection has the same data type. 
  * A generic collection enforces strong typing by allowing only the desired data type to be added. 
* System.Collections.Concurrent classes
  * Provide efficient thread-safe operations for accessing collection items from multiple threads.
  * Should be used whenever multiple threads are accessing the collection concurrently.
* System.Collections classes
  * These classes do not store elements as specifically typed objects, but as objects of type Object.

#### Enums

* An enumeration type (or enum type) is a value type defined by a set of named constants of the underlying integral numeric type.
* You use an enumeration type to represent a choice from a set of mutually exclusive values or a combination of choices. 
* To represent a combination of choices, define an enumeration type as bit flags.
* To define an enumeration type, use the `enum` keyword and specify the names of enum members.
* By default, the associated constant values of enum members are of type int; they start with zero and increase by one following the definition text order.
* You cannot define a method inside the definition of an enumeration type. To add functionality to an enumeration type, create an extension method.
* For any enumeration type, there exist explicit conversions between the enumeration type and its underlying integral type. 





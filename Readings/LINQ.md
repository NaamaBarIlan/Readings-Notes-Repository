# LINQ & Delegates

### Reading List:

##### [LINQ](https://docs.microsoft.com/en-us/dotnet/csharp/programming-guide/concepts/linq/)
##### [Introduction To LINQ Queries](https://docs.microsoft.com/en-us/dotnet/csharp/programming-guide/concepts/linq/introduction-to-linq-queries)
##### [Basic LINQ Query Operators](https://docs.microsoft.com/en-us/dotnet/csharp/programming-guide/concepts/linq/basic-linq-query-operations)
##### [Walkthrough Writing LINQ Queries in C#](https://docs.microsoft.com/en-us/dotnet/csharp/programming-guide/concepts/linq/walkthrough-writing-queries-linq)
##### C# 7.0 In a Nutshell - Chapter 8: LINQ Queries

---

### LINQ

* **Language-Integrated Query (LINQ)** is the name for a set of technologies based on the integration of query capabilities directly into the C# language. 
* Traditionally, queries against data are expressed as simple strings without type checking at compile time or IntelliSense support. Furthermore, you have to learn a different query language for each type of data source: SQL databases, XML documents, various Web services, and so on. 
* With LINQ, a query is a first-class language construct, just like classes, methods, events. You write queries against strongly typed collections of objects by using language keywords and familiar operators. 
* The LINQ family of technologies provides a *consistent query experience* for objects (LINQ to Objects), relational databases (LINQ to SQL), and XML (LINQ to XML).
* Query expressions are written in a declarative **query syntax**. By using query syntax, you can perform filtering, ordering, and grouping operations on data sources with a *minimum of code*.
* You can write LINQ queries in C# for SQL Server databases, XML documents, ADO.NET Datasets, and any collection of objects that supports `IEnumerable` or the generic `IEnumerable<T>` interface. 
* LINQ support is also provided by third parties for many Web services and other database implementations.

---

### Introduction to LINQ Queries

All LINQ query operations consist of three distinct actions:

1. Obtain the data source.
2. Create the query.
3. Execute the query.


### The Data Source

* A query is executed in a foreach statement, and foreach requires `IEnumerable` or `IEnumerable<T>`. 
* Types that support `IEnumerable<T>` or a derived interface such as the generic `IQueryable<T>` are called **queryable types**.
* A queryable type requires no modification or special treatment to serve as a LINQ data source. 
* If the source data is not already in memory as a queryable type, the LINQ provider must represent it as such. 

### The Query
* The query specifies what information to retrieve from the data source or sources.
* Optionally, a query also specifies how that information should be sorted, grouped, and shaped before it is returned. 
*  A query is stored in a query variable and initialized with a query expression.
*  The query expression contains three clauses: `from`, `where` and `select`.  
   *  The `from` clause - specifies the data source.
   *  The `where` clause - applies the filter.
   *  The `select` clause - specifies the type of the returned elements. 

### Query Execution

* **Deferred Execution** - the query variable itself only stores the query commands. The actual execution of the query is deferred until you iterate over the query variable in a foreach statement. 
* **Forcing Immediate Execution** - Queries that perform aggregation functions over a range of source elements must first iterate over those elements. 
  * Examples of such queries are `Count`, `Max`, `Average`, and `First`. 
  * These execute without an explicit foreach statement because the query itself must use foreach in order to return a result. 
  * These types of queries return a single value, not an `IEnumerable` collection. 


# Entity Framework Core & APIs

### Reading List:

##### [MVC with EF Get Started](https://docs.microsoft.com/en-us/aspnet/core/data/ef-mvc/intro?view=aspnetcore-3.1)
##### [Entity Framework Core](https://docs.microsoft.com/en-us/ef/core/)
##### [Data Seeding](https://docs.microsoft.com/en-us/ef/core/modeling/data-seeding)
##### [Razor Pages with Entity Framework Core](https://docs.microsoft.com/en-us/aspnet/core/data/ef-rp/intro?view=aspnetcore-2.1&tabs=visual-studio)
##### [Intro to APIs (video)](https://www.youtube.com/watch?v=aIkpVzqLuhA&feature=youtu.be)
##### [User Secrets](https://codefellows.github.io/code-401-dotnet-guide/Resources/UserSecrets.html)

---

### Entity Framework Core

* Entity Framework (EF) Core is a lightweight, extensible, open source and cross-platform version of the Entity Framework data access technology.
* EF Core can serve as an object-relational mapper (O/RM), enabling .NET developers to work with a database using .NET objects, and eliminating the need for most of the data-access code they usually need to write.
* EF Core supports many database engines, see Database Providers for details.

---

### Razor Pages

* Razor Pages is an aspect of ASP.NET Core MVC that makes coding page-focused scenarios easier and more productive.

---

### Asynchronous code

* A web server has a limited number of threads available, and in high load situations all of the available threads might be in use. When that happens, the server can't process new requests until the threads are freed up. 

* With synchronous code, many threads may be tied up while they aren't actually doing any work because they're waiting for I/O to complete. 

* With asynchronous code, when a process is waiting for I/O to complete, its thread is freed up for the server to use for processing other requests. As a result, asynchronous code enables server resources to be used more *efficiently*, and the server is enabled to handle more traffic without delays.

* Asynchronous code does introduce a small amount of *overhead* at run time, but for low traffic situations the performance hit is negligible, while for high traffic situations, the potential performance improvement is substantial.

---

### Data Seeding

* Data seeding is the process of populating a database with an initial set of data.

* There are several ways this can be accomplished in EF Core:

    * Model seed data
      * Seeding data can be associated with an entity type as part of the model configuration. Then EF Core migrations can automatically compute what insert, update or delete operations need to be applied when upgrading the database to a new version of the model.
      
    * Manual migration customization
      * When a migration is added the changes to the data specified with HasData are transformed to calls to InsertData(), UpdateData(), and DeleteData(). One way of working around some of the limitations of HasData is to manually add these calls or custom operations to the migration instead.
      
    * Custom initialization logic
      * A straightforward and powerful way to perform data seeding is to use DbContext.SaveChanges() before the main application logic begins execution.

* The seeding code should not be part of the normal app execution as this can cause concurrency issues when multiple instances are running and would also require the app having permission to modify the database schema.

---

###  User secrets

* User secrets is a secure way of storing private user information such as API keys, client secrets, and connection strings. Essentially anything that you don’t want others to know about when using your code base.

* The user secrets is not uploaded to any source control. This ensures your keys do in fact stay “secret” to your local machine.

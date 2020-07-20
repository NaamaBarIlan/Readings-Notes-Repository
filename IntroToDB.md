# Intro to Databases

### Reading List:

##### [Data Models (DB Schema)](https://www.tutorialspoint.com/dbms/dbms_data_schemas.htm)
##### [DBMS](https://www.tutorialspoint.com/dbms/dbms_overview.htm)

---

* **What is a Database Schema?**:
	* *What is a Schema?* 
	
		A database schema is the skeleton structure that represents the logical view of the entire database. 
		
		It defines how the data is organized and how the relations among them are associated. 
		
		It formulates all the constraints that are to be applied on the data.

		It contains a descriptive detail of the database, which can be depicted by means of schema diagrams.
	
	* *Why do we use them?*

		A database schema helps programmers understand the database and make it useful.

		
	* *What do they look like?*
		
		* **Physical Database Schema** − This schema pertains to the actual storage of data and its form of storage like files, indices, etc. It defines how the data will be stored in a secondary storage.

		* **Logical Database Schema** − This schema defines all the logical constraints that need to be applied on the data stored. It defines tables, views, and integrity constraints.

* ***What are the different types of Database Keys?***
	* *What is a Primary Key?*

		A Primary Key uniquely identifies each record in a table and must never be the same for the 2 records. Primary key is a set of one or more fields ( columns) of a table that uniquely identify a record in database table. A table can have only one primary key and one candidate key can select as a primary key. The primary key should be chosen such that its attributes are never or rarely changed
	
	* *What is a Foreign Key?*

		A Foreign Key is used to generate the relationship between the tables. Foreign Key is a field in database table that is Primary key in another table. A foreign key can accept null and duplicate value.
	
	* *What is a Composite Key?*

		A Composite Key is a combination of more than one attributes that can be used to uniquely identity each record. It is also known as “Compound” key. A composite key may be a candidate or primary key.
	
* ***What are Relationships in a relational database?***
	* *What is a 1:1 relationship?*

		In a one-to-one relationship, one record in a table is associated with one and only one record in another table. For example, in a school database, each student has only one student ID, and each student ID is assigned to only one person.
	
	* *What is a Many:Many relationship?*

		A many-to-many relationship occurs when multiple records in a table are associated with multiple records in another table. For example, a many-to-many relationship exists between customers and products: customers can purchase various products, and products can be purchased by many customers.

	* *How about a 1: Many or a Many:1?*
		
		In a one-to-many relationship, one record in a table can be associated with one or more records in another table. For example, each customer can have many sales orders.

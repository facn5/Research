# What is a schema and why/when would you need one?

---

The database schema of a database system is its structure described in a formal language supported by the database management system (DBMS). The term "schema" refers to the organization of data as a blueprint of how the database is constructed (divided into database tables in the case of relational databases). The formal definition of a database schema is a set of formulas (sentences) called integrity constraints imposed on a database.

---

# Primary Keys


---



A Primary Key is a column that uniquely identifies all table records.  

This serves as the 'key' to a relational database table.

It is usually an artifically generated id, but can also be an existing column of naturally-occuring data, like a birthday.


---



![Primary Key](https://dataedo.com/asset/img/kb/query/db2/tables_with_primary_keys.png)




---


## Why do you need a Primary Key?


![Retail Shelving](http://media.bizj.us/view/img/5215971/target-kailua-blessingnon-chilled-foods*750xx1200-675-0-63.jpg)


---



![call center](https://fortunedotcom.files.wordpress.com/2017/01/gettyimages-461116192.jpg)



---



A Primary Key’s main features are:

* Must contain a unique value for each row of data.
* It cannot contain null values.

Common Rules:

* Primary keys should be immutable: never changed or re-used.
* They should be deleted along with the associated record and not re-used.
* Primary keys should be anonymous integer or numeric identifiers.




---




## Primary Key in SQL

### On table creation:
```CREATE TABLE table_name (
id_col INT PRIMARY KEY,
col2 CHARACTER VARYING(20),
(etc)
)
```

### Alter existing table:
```ALTER TABLE [table identifier]
ADD [CONSTRAINT [constraint identifier] ]
PRIMARY KEY ([column expression] {, [column expression]... )
```


---



## Other Methods

Many developers and real-world situations require multiple primary-like keys, so hybrid "surrogate primary keys" are often used.

This is related to transferring Object-Oriented principles to the relational model, creating a hybrid "Object-Relational Model" or ORM, or "Active Record Pattern.


---




* The relational model (which comes from relational algebra and calculus) does not distinguish between primary and other kinds of keys.

* So Primary Keys were added to certain languages for convenience (i.e. PRIMARY KEY in SQL)

* There should still be as few main id columns as possible.




---




Active Record libraries are included in:
 
* ActiveJS for JavaScript
* ActiveRecord for PHP and Ruby
* Django for Python
* ActiveJDBC for Java

# MongoDB

Simply put, databases allow us to save and retrieve the data that we need.

Databases are typically `persisted` which means that even if our program stops or starts, we will still have access to the stored data.

Databases allow for:

- **Reliability**: Data can always be accessed.

- **Efficiency**: We could just use files to store the data, but this solution will be slow for any serious program.

- **Scalability**,: As our demands to get more and more data increases, databases also make it easy to increase our infrastructure capacity.

- **Concurrency**: We can have many clients connected to our database (program) simultaneously.

- **Data abstractions**: We can store data using complex data types that make it easy for us to save data without worrying about the underlying details of the implementation.

- **High-level query language**: Databases have a language in which we can ask them questions to get the data in whichever way we may need it.

While using the MEAN stack, we use MongoDB. 

MongoDB is a *non-relational* / *noSQL* database that stores data in collections. The data that is stored in `JSON` (JavaScript Object Notation) like documents that allow for changes to the structure.

>“For years, the primary method of working with data stores had been to issue SQL queries to relational databases. Yet there’s another type of data store that doesn’t rely on SQL. This class of database, known as NoSQL, doesn’t even use the familiar table structures of relational databases. NoSQL databases store data in a variety of formats, such as documents or key-value pairs, and are less rigid and structured than relational databases. This lack of structure often leads to simpler prototyping and ease of development. NoSQL databases tend to be slightly faster, as there’s no need for them to enforce the rigid table structure of relational databases.”



NoSQL databases store data in a variety of formats, such as documents or key-value pairs, and are less rigid and structured than relational databases. This lack of structure often leads to simpler prototyping and ease of development. NoSQL databases tend to be slightly faster, as there’s no need for them to enforce the rigid table structure of relational databases.

MongoDB is a document-oriented database that stores information as Binary JSON (BSON) documents. By using a flavor of JSON, Mongo is incredibly simple to read and write objects from JavaScript code. Just as Node replaces another server-side language with JavaScript, MongoDB replaces SQL with queries based on JavaScript objects. from [Full Stack JavaScript Development With MEAN - MongoDB, Express, AngularJS, and Node.JS 1st Edition](https://www.sitepoint.com/premium/books/full-stack-javascript-development-with-mean) by Colin J. Ihrig & Adam Bretz



*MongoDB Compass* is the official GUI (Graphical User Interface) for MongoDB.

`ObjectIDs` are a MongoDB type used to identify documents in a collection uniquely. MongoDB will create them automatically for us.

## C.R.U.D

![CRUD](https://i.imgur.com/CRowB2i.png)

CRUD = Create, Read, Update, Delete.

CRUD represents the four basic operations of any application which utilizes a database.

*Excerpts From: Adam Bretz, Colin J. Ihrig. “Full Stack JavaScript Development with MEAN.”*
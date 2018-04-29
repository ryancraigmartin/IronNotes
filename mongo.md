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

MongoDB is a non-relational database that stores data in collections. The data that is stored is in JSON like documents that allow for changes to the structure.

MongoDB Compass is the official GUI (Graphical User Interface) for MongoDB.

`ObjectIDs` are a MongoDB type used to identify documents in a collection uniquely. MongoDB will create them automatically for us.

## C.R.U.D

![CRUD](https://i.imgur.com/CRowB2i.png)

CRUD = Create, Read, Update, Delete.

CRUD represents the four basic operations of any application which utilizes a database.

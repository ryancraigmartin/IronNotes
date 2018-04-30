# Mongoose

Mongoose is a schema based solution to model your application data.

THe schema creates key value pairs for different data types.

## What does Mongoose do?

Mongoose creates an easy to use object reference when interacting with MongoDB. What makes mongoose great is that our database gets modeled within our code.

### How do we use Mongoose?

We first need to require the mongoose module and set a variable reference to a mongoose schema. Then we create a schema. In order to use our schema in other files, we need to create na instance of the schema . We call this instance a `model.` We can use our schema in other files by using the module.exports method which is given to us bu Node.js and setting a requirement within our files. 

Once we have our Schema set up, we need to establish a connection to MongoDB. We do this by creating a variable set to an instance of the database:

``` js
var myDB = 'mongodb://localhost/dbName';
```

Then we use mongoose.connect to establish the connection.

``` js
mongoose.connect(myDB);
```

## Mongoose Schema

The creation and usage of Schemas is the most used aspect of mongoose.

Schema and model are interchangeable.

You can think of a model as the basis for a database architecture. Each schema that we build will have a designated file structure associated with it.

### Example

``` js 
var mongoose = require('mongoose');
var Schema = mongoose.Schema;

var BookSchema = mongoose.Schema;
BookSchema = new Schema ({
  title: String; // Implicitly sets the type of data to String.
  author: {
    type: String,
    required: true, // Requires this entry.
  }
  published: {
    type: Date,
    default: Date.now // Adds a default value if a value is not passed.
  }
})

module.exports = mongoose.model("Book", BookSchema);
```
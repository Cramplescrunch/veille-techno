# Documentation sur l'installation et l'utilisation de MongoDB

## Installation

Pour l'installation, tout est expliqué sur le site de MongoDB à l'adresse suivante : https://docs.mongodb.com/manual/tutorial/install-mongodb-on-windows/

## Documentation

### Run MongoDB as a service

Quote from [this StackOverflow answer](https://stackoverflow.com/questions/52068925/what-does-it-mean-to-install-mongodb-as-a-service) : 

> *What are services?*
> 
> Services are application types that run in the system's background. These are applications such as task schedulers and event loggers. If you look at the Task Manager > Processes, you can see that you have a series of Service Hosts which are containers hosting your Windows Services.
> 
> *What difference does setting MongoDB as a service make?*
> 
> Running MongoDB as a service gives you some flexibility with how you can run and deploy MongoDB. For example, you can have MongoDB run at startup and restart on failures. If you don't set MongoDB up as a service, you will have to run the MongoDB server every time.
> 
> *So, what is the difference between a network service and a local service?*
> 
> Running MongoDB as a network service means that your service will have permission to access the network with the same credentials as the computer you are using. Running MongoDB locally will run the service without network connectivity.

### Run MongoDB from the Command Interpreter (not as a service)

#### 1. Create database directory

Create the data directory where MongoDB stores data. MongoDB's default data directory path is the absolute path \data\db on the drive from which you start MongoDB.

From the Command Interpreter, create the data directories:
(Windows)
```
cd C:\
md "data\db"
```

#### 2. Start your MongoDB database

To start MongoDB, run mongod.exe : 
(Windows)
```
"C:\Program Files\MongoDB\Server\4.0\bin\mongod.exe" --dbpath="C:\data\db"
```

If the MongoDB database server is running correctly, the Command Interpreter displays :
```
[initandlisten] waiting for connections
```

#### 3. Connect to MongoDB

To connect a mongo.exe shell to the MongoDB instance, open another Command Interpreter with Administrative privileges and run:

```
"C:\Program Files\MongoDB\Server\4.0\bin\mongo.exe"
```

## Memo

### Connect to the database (provided that MongoDB is already running) :
```
"<mongodb installation dir>\bin\mongo.exe"
"<mongodb installation dir>\bin\mongo.exe --port XXXX"
```

With MongoDB Instance on a Remote Host
```
"<mongodb installation dir>\bin\mongo.exe mongodb://mongodb0.example.com:28015"
"<mongodb installation dir>\bin\mongo.exe --host mongodb0.example.com:28015"
"<mongodb installation dir>\bin\mongo.exe --host mongodb0.example.com --port 28015"
```

MongoDB Instance with Authentication
```
"<mongodb installation dir>\bin\mongo.exe --host mongodb://alice@mongodb0.examples.com:28015/?authSource=admin"
"<mongodb installation dir>\bin\mongo.exe --username alice --password --authenticationDatabase admin --host mongodb0.examples.com --port 28015"
```

### Use the Mongo Shell

Display the database :
```
db
```

Switch database :
```
use <database>
```

To list the databases available to the user, use the helper `show dbs`.

When you first store data in the database, such as by creating a collection, MongoDB creates the database. 
The following creates both the database myNewDatabase and the collection myCollection during the insertOne() operation:
``` 
use myNewDatabase
db.myCollection.insertOne( { x: 1} );
```  

#### Insert Documents

`db.collection.insertMany()` can insert multiple documents into a collection. Pass an array of documents to the method.
Example : 
```
db.inventory.insertMany([
   // MongoDB adds the _id field with an ObjectId if _id is not present
   { item: "journal", qty: 25, status: "A",
       size: { h: 14, w: 21, uom: "cm" }, tags: [ "blank", "red" ] },
   { item: "notebook", qty: 50, status: "A",
       size: { h: 8.5, w: 11, uom: "in" }, tags: [ "red", "blank" ] },
   { item: "paper", qty: 100, status: "D",
       size: { h: 8.5, w: 11, uom: "in" }, tags: [ "red", "blank", "plain" ] },
   { item: "planner", qty: 75, status: "D",
       size: { h: 22.85, w: 30, uom: "cm" }, tags: [ "blank", "red" ] },
   { item: "postcard", qty: 45, status: "A",
       size: { h: 10, w: 15.25, uom: "cm" }, tags: [ "blue" ] }
]);
```

## Links and sources 

- Installation : https://docs.mongodb.com/manual/tutorial/install-mongodb-on-windows/#run-mongodb-from-cmd
- MongoDB as a service (StackOverflow) : https://stackoverflow.com/questions/52068925/what-does-it-mean-to-install-mongodb-as-a-service 
- Manual / Mongo Shell : https://docs.mongodb.com/manual/mongo/

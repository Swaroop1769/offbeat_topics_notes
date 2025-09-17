Angular is a framework which allows us to create single page application.

Components: are a key feature...you build these components on your own...(root component/app component eg: sidebar components)

Decorators: are typescript feature...allows to enhance the classes...decorators are always attached by adding '@' sign before the component.




Mongo Db: Humongous onne...as it can store lots and lots of data...not only storing..you can work efficiently on the data that's stored.
Mongo Db is highly efficient and enables us to store data in a logical way.
Mongo Db advantage: Flexibility and optimization of usability.
###

Mongo DB uses BSON format instead of JSON format behind the scenes....it stores data in Binary format.
But we write in JSON and the output is displayed in JSON...internally it is converted into BSON with the help of Mongo DB drivers.
It is done as converting into BSON and storing it is efficient compared to JSON

###
How Mongo Db Works:

in object format: Database --> Collections --> Documents( inside a document you can be schemaless which is flexible compared to others like postgres etc.)

Mongo Db is a noSQL solution

less tables(collections) but data is stored together...which is quite helpful...No need to move from collection A to B..instead it searches for document..which makes it more flexible.


Mongo DB Ecosystem:
Stich...gives serverless query API...to query efficiently directly from client side apps
main motive of Mongo DB: which will be used in CLoud(Atlas) and Locally, how to perform crud operations, to retrive data efficiently

commands used in Mongo DB Shell:
cls: clear screen
show dbs: displays the current databases
use: command used to connect to a database
db.database_name.insertOne({name: " A Book ", price: 12.00})   ## for this the document gets created using the name and price....so after this gets executed we get acknowledged with True/False and unique object ID is created
db.database_name.find()....this returns all the items present in document with object ID's...##db.database_name.find().pretty()


Mongo DB Drivers: packages for different programming languages...bridges for programming lang and mongo db server
The drivers will interact with Mongo DB servers

Working with Mongo DB Servers:::

Application Layer:  1)Front-End   2)Back-End.... in this there'll be drivers

Data Layer:   Mongo DB servers <----communicates----> Storage Engine (Wired Tiger is great Storage Engine)

[[ Drivers or Mongo DB Playshell--->Queries---->Mongo DB server <----communicates---> Storage Engine <----> stores files/Data Access ]]

 
Document and CRUD Operations...[Create, Read, Update, Delete]

Databases, Collections, Documents are linked::: these three are created implicitly i.e when you create database automatically these are created..
In Database----> number of Collections ----> in each collections(a collection would be a table in SQL DB) there are number of documents(data pieces)


Create:                                                    Update:

   insertOne(data, options)                                      updateOne(filter, data, options)
   insertMany(data,options)                                      updateMany(filter, data, options)
                                                                 replaceOne(filter, data, options)



Read:                                                      Delete:

    find(filter, options)                                        deleteOne(filter, options)
    findOne(filter, options)                                     deleteMany(filter, options)

"$"----> whenever we see $ symbol in Mongo DB it means that it is a reserved word.
"$gt"-----> resembles greater then 

"find" command doesnot give us an array of objects...instead it gives us cursor object which gives a lot of metadata..that allows us to cycle through the results...

Schema:: Schema means structure of one document...so it's totally fine to mix 2 different schemas in Mongo DB
Without schema it's not possible...there's some kind of schema for an application...as our data requires some or the other form...how will our data look like?



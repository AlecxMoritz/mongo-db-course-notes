# Module One

## Getting Started

Mongo is really a huge ecosystem for development.

There is the Mongo Server, which houses the databases and data, and the Shell, where you can interact with those databases.

Mongo Server is not running by default and will need to be started before you can start the Shell.

#### Commands

`mongod` - Starts the Mongo Server

`mongo` - Starts the shell, and connects to Mongo Server

Note: Make sure to keep the server process open or the shell cannot connect to the database.

## Basic Shell User

The shell is where all contact with the databases is made, or the Mongo Server itself. You can create new databases, collections, and perform CRUD functions, aggregates, set up new users and more directly from the shell.

#### Commands

`cls` - Clears the screen

`show dbs` - prints all available databases on the server

- Mongo comes with three default databases as well: admin, config, and local

`use shop` - sets the shell to use a certain database, here `shop` is the name of a database

- The `use` command will also create the database for you if need be. Think of this as like temporary creation though, as you will need insert data before the database is really created.

`db.products.insert({ ... })` - There are many parts to this.

- After using `use shops`, `db` now refers to the `shop` database.
- `products` is the name of a collection. Similar to `use`, you do not have to create this collection before trying to access it. This command is capable of creating the collection _and_ adding the document to it.

`db.products.find()` - Finds and returns _all_ documents in the specific collection, again here `products`.

- There is a slight variant you can use to get the documents in the collection to display in a more human eye friendly way.
  `db.products.find.pretty()`

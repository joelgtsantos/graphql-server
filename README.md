# graphql-server
Setting up a GraphQL Server

Setting up from scratch a GraphQL Server. It runs in a HTTP port the GraphiQL console which is connected to a basic SQLite Schema. All of the things that can be tested from the console are simple Graphql queries, Cursor-based pagination, Mutations. Besides the app works with a authentication to run the queries.

The data base schema is compose by three tables.

users

| Column    | Type          |
| --------- |:-------------:|
| id        | Integer       |
| name      | Text          |
| about     | Text          |

usersFriends

| Column    | Type          |
| --------- |:-------------:|
| user_id_a | int           |
| user_id_b | int           |
| level     | Text          |

posts

| Column    | Type          |
| --------- |:-------------:|
| id        | INTEGER       |
| user_id   | int           |
| body      | text          |
| level     | text          |
| created_at| datetime      |


## How to run

### Install Dependencies
1. Npm install

### Install SQLite Schema
1. $ node -e 'require("babel-register"); require("./src/seedData");'

### Run 
1. $ node server.js

https://www.youtube.com/watch?v=ZQL7tL2S0oQ

_______________REST_____________
- fetch URL and it returns json full of data
- post, get, delete





__________________GraphQL_________________
- query language
- instead of URL you ask for specific kind of data
- one single ENDPOINT API

- can create, read, update, delete 

- no need for /editionId/schedule



///////////////////////////////////////////////////////////
1. DESCRIBE YOUR DATA

type Project {
  name: String
  tagline: String
  contributors: [User]
}


2. ASK FOR WHAT YOU WANT

{
  project(name: "GraphQL") { // project where name is GraphQL
    tagline                 // and return tagline
  }
}


3. GET PREDICTABLE RESULTS

{
  "project": {
    "tagline": "A query language for APIs"  // returned tagline
  }
}




EXAMPLE of Describing 2.:


type Query {
  hero: Character
}

type Character {
  name: String
  friends: [Character]
  homeWorld: Planet
  species: Species
}

type Planet {
  name: String
  climate: String
}

type Species {
  name: String
  lifespan: Int
  origin: Planet
}




//////////////////////////////////////////////////////////////////
Send a GraphQL query to your API and get exactly what you need

1. QUERY

{
  hero {
    name
    height
  }
}


2. RETURNS

{
  "hero": {
    "name": "Luke Skywalker",
    "height": 1.72
  }
}



///////////////////////////////////////////////////////////////////
///////////////////////////////////////////////////////////////////
____________________NET NINJA_____________________


//////////////////////////////////
REST Get all books:
domain.com/books

REST Get single book:
domain.com/books/:id
/////////////////////////////////


GraphQL:
- instead of URL you ask for specific kind of data
- one single ENDPOINT API


{
book(id: 123) {          // book
title
genre
reviews
author {             // author
name
bio
books {          // author books
name
}
}
}
}



// FRONTENT QUERY:

queries/ query.js


import { gql } from ..


const getAuthorsQuery = gql`
{
authors {
name
id
}
}
`;



Queries and Mutations
https://graphql.org/learn/queries/


__________________________________________________________________________________________

1. creating express to listen for REQUESTS on port
https://www.youtube.com/watch?v=ZOHIZXRfvVY&list=PL4cUxeGkcC9iK6Qhn-QLcXCXPQUov1U7f&index=5



2. ONE ENDPOINT to rule them all 
https://www.youtube.com/watch?v=pH02J0U5OBI&list=PL4cUxeGkcC9iK6Qhn-QLcXCXPQUov1U7f&index=6



3. SCHEMA to deal with data
https://www.youtube.com/watch?v=A8vtRvz-lK0&list=PL4cUxeGkcC9iK6Qhn-QLcXCXPQUov1U7f&index=7

-> object types(books, authors), relationships
-> schema/schema.js


const BookType = new GraphQLObjectType({  // defined object 
name: 'Book',
fields: () => ({
id: { type: GraphQLString },
name: { type: GraphQLString },
genre: { type: GraphQLString }
})
}); 



4. defining ROOT queries so user grabs data (slika)
https://www.youtube.com/watch?v=ALqNbTik44o&list=PL4cUxeGkcC9iK6Qhn-QLcXCXPQUov1U7f&index=8

-> inside schema.js


const RootQuery = new GraphQLObjectType({   // defining query
name: 'RootQueryType',
fields: {                   // queries
book: {                 // name of frontend query
type: BookType,
args: { id: { type: GraphQLString }} //  // book(id: 123) arguments when looking for specific book using ID string
resolve(parent, args) { 
// code to return data from DB

}
},
author: {
......
......
resolve(parent, args){
...
}
}                                        
}
});



5. The Resolve Function
https://www.youtube.com/watch?v=NWod5SFW13s&list=PL4cUxeGkcC9iK6Qhn-QLcXCXPQUov1U7f&index=9
https://www.youtube.com/watch?v=Pe1MgqWFyYE&list=PL4cUxeGkcC9iK6Qhn-QLcXCXPQUov1U7f&index=12

// dummy data

var books = [
{name: 'Wild wild west', genre: 'fantasy', id: '1'},
{name: 'Wcvn', genre: 'fantasy', id: '2'}
{name: 'cvnn', genre: 'fantasy', id: '3'}
]



resolve(parent, args) { // take ID from args and look at books array
// code to get data from DB
return _.find(books, {id: args.id}); // LODASH
}



6. Testing
https://www.youtube.com/watch?v=5RGEODLhjhY&list=PL4cUxeGkcC9iK6Qhn-QLcXCXPQUov1U7f&index=10



// FRONTENT QUERY:

queries/query.js


import { gql } from ..


const getBooksQuery = gql`
{
book(id: "1") {
name
genre
}
}
`;

---------- WE GET BACK ----------


{
"data": {
"book": {
"name": "Wild wild west",
"genre": "fantasy"
}
}
}

`

__________________________________________________________________________________________
                          RELATIONSHIPS - book author

book has specific author:


// dummy data

var books = [
{name: 'Wild wild west', genre: 'fantasy', id: '1', authorId: '1'}, //authorId
{name: 'Wcvn', genre: 'fantasy', id: '2', authorId: '2'}
{name: 'cvnn', genre: 'fantasy', id: '3', authorId: '3'}
]

var authors = [  // passing this to RESOLVE
{name: 'aaaaaaa', age: 11, id: '1'}, 
{name: 'bbbb', age: 21, id: '2'}
{name: 'cccc', geagenre: 32, id: '3'}
]


const BookType = new GraphQLObjectType({   
name: 'Book',
fields: () => ({
id: { type: GraphQLString },
name: { type: GraphQLString },
genre: { type: GraphQLString },
author: { 
type: AuthorType,   // created similar to BookType
resolve(parent, args){  // tell what author coresponds to book
return _.find(authors, {id: parent.authorId}); // LODASH
// parent = book.authorId (requested book)
}},

})
}); 


// FRONTEND QUERY:

queries/query.js


import { gql } from ..


const getBookAuthorQuery = gql`
{
book(id: "2") {
name
genre
author{      // new query
name
age
id
}
}
}
`;

---------- WE GET BACK ----------


{
"data": {
"book": {
"name": "Wild wild west",
"genre": "fantasy",
"author": {
"name": "bbbb",
"age": 21,
"id": "2"
}
}
}
}

`

____________________________________________________________________________________
MUTATIONS


https://graphql.org/learn/queries/#mutations
https://www.youtube.com/watch?v=DU77lbBPfBI&list=PL4cUxeGkcC9iK6Qhn-QLcXCXPQUov1U7f&index=18
- add, delete, edit 



schema.js


const Mutation = new GraphQLObjectType({   
name: 'Mutation',
fields: () => ({
addAuthor: {
type: AuthorType,
args: { // arguments about NEW ADDED AUTHOR
name: {type: GraphQLString},
age: {type: GraphQLInt}
},
resolve(parent,args){
let author = new Author({        // imported model mongoose
name: args.name
age: args.age
});
return author.save()     // mongoose save to database and return
}
}
})
}); 




// FRONTEND MUTATION:

mutation {
addAuthor(name: "Shaun", age: 30){   // data to send
name   // data to get back
age   // data to get back
}
}



---------- WE GET BACK ----------


{
"data": {
"addAuthor": {
"name": "Shaun",
"age": 30
}
}
}

__________________________________________________________________________________
                            graphql apollo react

https://www.youtube.com/watch?v=SEMTj8w04Z8
https://www.youtube.com/watch?v=-XwkFm5a9lw&list=TLPQMTUwNDIwMjCobKF2p195gA&index=2


----- APOLLO -----

const express = require('express');
const { ApolloServer, gql } = require('apollo-server-express');

const typeDefs = gql`     // defining object structure
  type Query {
    hello: String
  }
`;



const resolvers = {        // setting object data?
  Query: {
    hello: () => 'Hello world!',
  },
};

const server = new ApolloServer({ typeDefs, resolvers });

const app = express();
server.applyMiddleware({ app });

app.listen({ port: 4000 }, () =>
  console.log('Now browse to http://localhost:4000' + server.graphqlPath)
);

///////////////////////////////////////////////////////


INSIDE COMPONENT:

const LAUNCHES_QUERY = gql`
query LaunchesQuery {
launches {
flight_number
mission_name
}
}
`;

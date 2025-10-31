# Assingment-2 For Big Data Management and Processing Course COMP-548DL
The data model implementation is on MongoDB Atlas. 
I've created a Read_user in order to access the database (used compass) and allowed the IP address access to be from anywhere. So you can connect via the connection string below.

## Connection
Connection String: "mongodb+srv://Read_user:Assignment@cluster0.rxdbvnd.mongodb.net/"

## Implementations
- I've created 2 collection of documents for Users and Documents.
- They are in JSON format.
- Uploaded 2 files, examples for Users and Documents documents used. 
- The database have 20 users and 5 documents
- Each User document has information about the user and each Document document has information about the document like title,id while also the collaborators on that document and the different edits applied.
- The queries that can be performed is:
   - find and get User information
   - find and get User Document information 
   - find collaborators worked on document
   - find the edits on a document(along with what and who edited)
   - find specific edits of a document

## Examples of queries
Find specific User
- db.Users.find({user_id:1})

Find users with id between 1 and 10
- db.Users.find( { user_id: {$gte:1,$lte:10}})

Find a specific document
- db.Documents.find({doc_id:2})

Find only the collaborators of a specific document
- db.Documents.find({doc_id:1},{collaborators:1})

Find only the edits of a specific document
- db.Documents.find({doc_id:1},{document_edits:1})

Find a specific edit of a document
- db.Documents.find({doc_id:1,"document_edits.edit_id":"d12"},{"document_edits.$": 1})


# Objective: To Build a Simple CRUD API with Go

## UseCase - Library Management System

These APIs are used to manage books in the library and it uses CRUD operations.

- **Create:** Add a new book to the library by entering the ID, Title, Description. The availability status of a book is set as "Pending" by default.
- **Read:** List all available books that have been created or search for a specific book by its ID.
- **Update:** Set the status of a book as available or pending or update its information (Topic/Description).
- **Delete:** Remove a book from the library management system.

### HTTP Server Status:

![Server-Status](https://github.com/ponnisajeevan12/w6_go_2/blob/master/images/Server-Status.png)

### 1) Add a Book : POST

```
$ curl -X POST http://localhost:8000/book -H "Content-Type: application/json" -d '{"id":"1", "title":"M06", "description":"ProgrammingwithGO"}'
$ curl -X POST http://localhost:8000/book -H "Content-Type: application/json" -d '{"id":"2", "title":"CloudComputing", "description":"AWS Administration", "status":"Available"}'
$ curl -X POST http://localhost:8000/book -H "Content-Type: application/json" -d '{"id":"3", "title":"AZ-104", "description":"Azure Administration", "status":"Available"}'
```
![Create-Book](https://github.com/ponnisajeevan12/w6_go_2/blob/master/images/Create-Book.png)

### 2) List All Books :  GET

```
$ curl http://localhost:8000/book
```
![List-All-Book](https://github.com/ponnisajeevan12/w6_go_2/blob/master/images/List-All-Books.png)

### 3) List Book by ID : GET

```
$ curl http://localhost:8000/book/1
$ curl http://localhost:8000/book/2
```
![List-All-Book-By-ID](https://github.com/ponnisajeevan12/w6_go_2/blob/master/images/List-Book-ByID.png)
![List-All-Book-By-ID](https://github.com/ponnisajeevan12/w6_go_2/blob/master/images/List-Book-By-ID.png)

### 4) Update the Status of the Book : PUT

```
$ curl -X PUT http://localhost:8000/book/1 -d '{"status":"Available"}' -H "Content-Type: application/json"
```
![Change-Book-Availability](https://github.com/ponnisajeevan12/w6_go_2/blob/master/images/Update-BookStatus.png)
![Check-Availability-Status](https://github.com/ponnisajeevan12/w6_go_2/blob/master/images/Status-Updated.png)

### 5) Delete the Book: DELETE

```
$ curl -X DELETE http://localhost:8000/book/1
```
![Delete-Book-Availability](https://github.com/ponnisajeevan12/w6_go_2/blob/master/images/Delete-Book.png)
![Check-Book-Availability](https://github.com/ponnisajeevan12/w6_go_2/blob/master/images/BookDeleted-ID1.png)
![Extract-Book-By-ID-Error](https://github.com/ponnisajeevan12/w6_go_2/blob/master/images/Extract-WrongID.png)
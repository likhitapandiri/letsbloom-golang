# letsbloom-golang
This project is a simple Go application that serves as a RESTful API for managing a book library.The Go code is in a file named main.go .
Using gin web framework for building api end points and initialized a connection to a MySQL database to store and retrieve book information.
Created a simple RESTful API with endpoints for handling GET, POST, and PUT requests in managing the library system. 
The file includes the handlers for GET, PUT, POST methods.
Created a database using mysql which includes a table named Book which has columns of id, name,author_name,published_date,image_url, and location.

How to run:

Commands : 

cd folder_name

go mod tidy

go run main.go

1) Posting a New Book data.
   
Endpoint: {/api/books}

Method: POST

Description: Posting a new book by sending a JSON payload with the book details in the request body.Using the BindJSON method to bind the incoming JSON payload to models. Book struct and then insert the data into the database.

2) Get Book by ID

Endpoint: /api/books

Method: GET

Description: Retrieves all rows from the Book table and returns a JSON response containing the book data.

3) Update an Existing Book

Endpoint: /api/books/{id}

Method: PUT

Description: Extracting the book ID from the request parameters, binds the incoming JSON payload to a models. Book struct, and dynamically generates the SQL update query based on the provided fields.


Dependencies used are
Gin: Web framework for Go and 
Go MySQL Driver: MySQL driver for Go.

# letsbloom-golang
The go code is in a file named main.go .
Setted up Go web application using the gin framework and initialized a connection to a MySQL database
Created a simple RESTful API with endpoints for handling GET, POST, and PUT requests in managing the library system. 
The file includes the handlers for GET, PUT, POST methods.
Created a database using mysql which includes a table named Book which has columns of id, name,author_name,published_date,image_url, and location.

1) Posting a New Book data.
Endpoint: {/api/books}
Method: POST
Description: Posting a new book by sending a JSON payload with the book details in the request body.Using the BindJSON method to bind the incoming JSON payload to models. Book struct and then insert the data into the database.

3) Get Book by ID
Endpoint: /api/books
Method: GET
Description: Retrieves all rows from the Book table and returns a JSON response containing the book data.

4) Update an Existing Book
Endpoint: /api/books/{id}
Method: PUT
Description: Extracting the book ID from the request parameters, binds the incoming JSON payload to a models. Book struct, and dynamically generates the SQL update query based on the provided fields.

# BooksAPI---PostMan  

Documentation Link:- https://documenter.getpostman.com/view/23631937/2s9YeD9ZHw
<br>
![e](https://github.com/Brijesh-Singh-git/BooksAPI---PostMan/assets/106757278/e1ee3021-2554-4e8a-802b-5634fab39c7b)
<br>
# Simple Books API #

This API allows you to reserve a book.

The API is available at `https://simple-books-api.glitch.me`

## Endpoints ##

### Status ###

GET `/status`

Returns the status of the API.

### List of books ###

GET `/books`

Returns a list of books.

Optional query parameters:

- type: fiction or non-fiction
- limit: a number between 1 and 20.


### Get a single book ###

GET `/books/:bookId`

Retrieve detailed information about a book.


### Submit an order ###

POST `/orders`

Allows you to submit a new order. Requires authentication.

The request body needs to be in JSON format and include the following properties:

 - `bookId` - Integer - Required
 - `customerName` - String - Required

Example
```
POST /orders/
Authorization: Bearer <YOUR TOKEN>

{
  "bookId": 1,
  "customerName": "John"
}
```

The response body will contain the order Id.

### Get all orders ###

GET `/orders`

Allows you to view all orders. Requires authentication.

### Get an order ###

GET `/orders/:orderId`

Allows you to view an existing order. Requires authentication.

### Update an order ###

PATCH `/orders/:orderId`

Update an existing order. Requires authentication.

The request body needs to be in JSON format and allows you to update the following properties:

 - `customerName` - String

 Example
```
PATCH /orders/PF6MflPDcuhWobZcgmJy5
Authorization: Bearer <YOUR TOKEN>

{
  "customerName": "John"
}
```

### Delete an order ###

DELETE `/orders/:orderId`

Delete an existing order. Requires authentication.

The request body needs to be empty.

 Example
```
DELETE /orders/PF6MflPDcuhWobZcgmJy5
Authorization: Bearer <YOUR TOKEN>
```

## API Authentication ##

To submit or view an order, you need to register your API client.

POST `/api-clients/`

The request body needs to be in JSON format and include the following properties:

 - `clientName` - String
 - `clientEmail` - String

 Example

 ```
 {
    "clientName": "Postman",
    "clientEmail": "valentin@example.com"
}
 ```

The response body will contain the access token. The access token is valid for 7 days.

**Possible errors**

Status code 409 - "API client already registered." Try changing the values for `clientEmail` and `clientName` to something else. 

<br> <br> 
<p> ---------------------------------------------------------------------------------------------------------------------------------------</p>

![1](https://github.com/Brijesh-Singh-git/BooksAPI---PostMan/assets/106757278/48992f0d-bfc2-459a-91bf-c2d52307c06c)
<br>
 ![2](https://github.com/Brijesh-Singh-git/BooksAPI---PostMan/assets/106757278/6dba3715-a095-470c-9206-2bac588dd282)
<br>
![3](https://github.com/Brijesh-Singh-git/BooksAPI---PostMan/assets/106757278/5067aa32-4d21-4633-93ed-27197e435494)
<br>
![4](https://github.com/Brijesh-Singh-git/BooksAPI---PostMan/assets/106757278/c6886ace-eb72-4e93-b333-19b13f0077a6)

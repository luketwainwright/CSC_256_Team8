#   Wake County Bookstore API Documentation

Welcome to the Wake County Bookstore. This API allows developers to access and interact with our online bookstore's features, including browsing books, managing a shopping cart, placing orders, and viewing order history.

## Base URL

The base URL for all API endpoints is: `http://127.0.0.1:3000`

## Authentication

Authentication is required to access specific API endpoints. We use API keys for authentication. To obtain an API key, please get in touch with our support team.

### Request Headers 

 `Authorization: Bearer YOUR_API_KEY`   -***-future implementation***

## Endpoints 
 Get the yaml representation using the openAPI 3.0 specification format here.***[wc-booksore.yaml](./wc-booksore.yaml)***
### List Books

 **Endpoint:** `/api/books` \
 **HTTP Method:** GET \
 **Description:** Get a list of books available in the bookstore. \
 **Parameters:** 
  - `search` : A search query to filter books by title, author, or genre. \
  - `category`: Filter books by category or genre. \
 **Response:** 
    - **Status Code:** 200 OK 
    - **Body:** JSON array containing book objects. Example response: 

```json
  [
    {
        "authors": "Marilynne Robinson",
        "categories": "Fiction",
        "num_pages": "247",
        "published_year": "2004",
        "subtitle": "",
        "title": "Gilead"
    },
    {
        "authors": "Charles Osborne;Agatha Christie",
        "categories": "Detective and mystery stories",
        "num_pages": "241",
        "published_year": "2000",
        "subtitle": "A Novel",
        "title": "Spider's Web"
    },
  ]
```

- **Status Code:** 500 OK

### Display single Book 

 **Endpoint:** `/api/books/{book_id}` \
 **HTTP Method:** GET \
 **Description:** Get detailed information about a specific book. \
 **Parameters:** \
   `book_id` : The unique identifier of the book. \
 **Response:** 
  - **Status Code:** 200 OK 
  - **Body:** JSON array containing book objects. Example response: 

  ```json
  {
  "id": "1",
  "title": "The Great Gatsby",
  "author": "F. Scott Fitzgerald",
  "price": 10.99,
  "description": "A classic novel...",
  "category": "Fiction"
  }
 ```

### Add Book to Cart 

 **Endpoint:** `/api/cart/add`  \
 **HTTP Method:** POST \
 **Description:** Add a book to the user's shopping cart. \
 **Response:** 
  - **Status Code:** 201 Created 
  - **Body:** Confirmation message. 
  - **Body:** JSON object containing book_id and quantity. 
  
```json
  {
  "book_id": "1",
  "quantity": 2
  }

```

### View Cart 
**Endpoint:** `/api/cart` \
**HTTP Method:** GET \
**Description:** Get the user's shopping cart contents. \
**Response:** 
  - **Status Code:** 200 OK 
  - **Body:** JSON array of cart items. 

  ```json
    [
        {
            "book": {
            "id": "1",
            "title": "The Great Gatsby",
            "author": "F. Scott Fitzgerald",
            "price": 10.99
            },
            "quantity": 2
        }
    ]
  ```

### Remove Book from Cart 
**Endpoint:** /cart/remove/{book_id} \
**HTTP Method:** DELETE \
**Description:** Remove a book from the user's shopping cart. \
**Parameters:** 
`book_id`: The unique identifier of the book. \
**Response:** 
  - **Status Code:** 204 No Content 

### Place an Order 
**Endpoint:** /orders/place \
**HTTP Method:** POST \
**Description:** Order the books in the user's shopping cart. \
**Request Body:** 
- JSON object containing user and payment information. Example request body: 
  
```json 
{
  "userId": "12345",
  "items": [
    {
      "book_id": "1",
      "quantity": 2
    }
  ],
  "payment": {
    "cardNumber": "**** **** **** 1234",
    "expiryDate": "12/25",
    "cvv": "123"
  }
}

```
**Response:** 

- **Status Code:** 201 Created 
- **Body:** Order confirmation with order ID. Example response: 

```json 
{
  "orderId": "ABC123",
  "totalAmount": 21.98
}

```
### View Order History 
**Endpoint:** /orders \
**HTTP Method:** GET \
**Description:** Get the user's order history. \
**Response:** 
- **Status Code:** 200 OK
- **Body:** JSON array of order objects. Example response:
```json

[
  {
    "orderId": "ABC123",
    "orderDate": "2023-11-15T12:34:56Z",
    "items": [
      {
        "book": {
          "id": "1",
          "title": "The Great Gatsby",
          "author": "F. Scott Fitzgerald",
          "price": 10.99
        },
        "quantity": 2
      }
    ],
    "totalAmount": 21.98
  }
]
```

### Get Categories 
**Endpoint:** /categories \
**HTTP Method:** GET \
**Description:** Get a list of available book categories or genres. \
**Response:**
- **Status Code:** 200 OK
- **Body:** JSON array of category objects. Example response:
```json
[
  "Fiction",
  "Non-Fiction",
  "Mystery",
  "Science Fiction"
]
```

### Error Handling

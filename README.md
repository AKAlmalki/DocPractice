# API Documentation Practice
In this exercise, your task is to practice writing documentation for the bookstore app we created earlier.

You'll soon be writing documentation for your final project (the Trivia API), after which you'll get feedback from a reviewer. You can think of this as some rudimentary practice to prepare for that.

At each step, you can compare what you've written with our own version. Of course, **there isn't a single correct way to write a piece of documentation**, so your version may look quite different. However, there are principles and practices you should follow in order to produce quality documentation, and we'll point this out so you can check whether you've incorporated them in what you wrote.

## Getting started

- Base URL: This version of app can only be run locally, the backend app is hosted at the default:
```bash
http://127.0.0.1:5000
## which is set as a proxy in the frontend configuration.
```
- Authentication: This version the application doesn't require any authentication or API keys.


## Error Handling

In our API, uses conventional JSON objects to indicate the success or failure of an API request. It will return json response with a body that have the following attributes:
- `error`: indicate the HTTP status code.
- `message`: indicate a short description for the error type.
- `success`: indicate the success or the failure of the request.

#### Not Found (404)
```bash
{
  "error": 404,
  "message": "resource not found",
  "success": false
}
```

#### Method Not Allowed (405)
```bash
{
  "error": 405,
  "message": "method not allowed",
  "success": false
}
```

#### Unprocessable (422)
```bash
{
  "error": 422,
  "message": "unprocessable",
  "success": false
}
```

#### Bad Request (400)
```bash
{
  "error": 400,
  "message": "bad request",
  "success": false
}
```



## Endpoint Library

### GET /books
- Description: retrieve all the books ordered by id.
- Results are paginated in groups of 8, include a request argument to choose page number (start from 1)

#### JSON Response body
```bash
{
  "success": True,
  "books": current_books,
  "total_books": len(Book.query.all()),
}
```
#### Attributes
+ `success`: indicate the success or failure of the request.
+ `books`: paginated books list that is ordered by id.
+ `total_books`: the number of current books.

#### Sample `curl http://127.0.0.1:5000/books`
```bash
{
  "books": [
    {
      "author": "Stephen King",
      "id": 1,
      "rating": 5,
      "title": "The Outsider: A Novel"
    },
    {
      "author": "Lisa Halliday",
      "id": 2,
      "rating": 4,
      "title": "Asymmetry: A Novel"
    },
    {
      "author": "Kristin Hannah",
      "id": 3,
      "rating": 4,
      "title": "The Great Alone"
    },
    {
      "author": "Tara Westover",
      "id": 4,
      "rating": 5,
      "title": "Educated: A Memoir"
    },
    {
      "author": "Jojo Moyes",
      "id": 5,
      "rating": 5,
      "title": "Still Me: A Novel"
    },
    {
      "author": "Leila Slimani",
      "id": 6,
      "rating": 2,
      "title": "Lullaby"
    },
    {
      "author": "Amitava Kumar",
      "id": 7,
      "rating": 5,
      "title": "Immigrant, Montana"
    },
    {
      "author": "Madeline Miller",
      "id": 8,
      "rating": 5,
      "title": "CIRCE"
    }
  ],
  "success": true,
  "total_books": 16
}
```


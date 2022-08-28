# API Documentation Practice
In this exercise, your task is to practice writing documentation for the bookstore app we created earlier.

You'll soon be writing documentation for your final project (the Trivia API), after which you'll get feedback from a reviewer. You can think of this as some rudimentary practice to prepare for that.

At each step, you can compare what you've written with our own version. Of course, **there isn't a single correct way to write a piece of documentation**, so your version may look quite different. However, there are principles and practices you should follow in order to produce quality documentation, and we'll point this out so you can check whether you've incorporated them in what you wrote.

## Getting started
Now, add a Getting Started section to your documentation. Remember, this should include at least your base URL and an explanation of authentication. Feel free to provide other information that is relevant for your API

Getting started?
...

#### Base URL:
```bash
http://127.0.0.1:5000
```



## Error Handling
Now, add an Error Handling section to your documentation. It should include the format of the error responses the client can expect as well as which status codes you use.
- Response codes
- Messages
- Error types

In our API, uses conventional json response to indicate the success or failure of an API request. It will return json response with a body that have the following attributes:
- error: indicate the HTTP status code.
- message: indicate a short description for the error type.
- success: indicate the success or the failure of the request.

### Not Found (404)
```bash
## JSON Response
{
  "error": 404,
  "message": "resource not found",
  "success": false
}
```

### Method Not Allowed (405)
```bash
## JSON Response
{
  "error": 405,
  "message": "method not allowed",
  "success": false
}
```

### Unprocessable (422)
```bash
## JSON Response 
{
  "error": 422,
  "message": "unprocessable",
  "success": false
}
```

### Bad Request (400)
```bash
## JSON Response
{
  "error": 400,
  "message": "bad request",
  "success": false
}
```



## Endpoint Library
Now, add an Endpoint Library section to your documentation. Make sure that endpoints, methods and returned data are all clear. Consider including sample requests for clarity

- Organized by resource
- Include each endpoint
- Sample request 
- Arguments including data types
- Response object including status codes and data types 

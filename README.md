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
Now, add an Endpoint Library section to your documentation. Make sure that endpoints, methods and returned data are all clear. Consider including sample requests for clarity

- Organized by resource
- Include each endpoint
- Sample request 
- Arguments including data types
- Response object including status codes and data types 

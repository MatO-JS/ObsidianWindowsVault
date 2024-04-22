
### Format of an HTTP request 

The HTTP request from the client is a message sent to a server by a client requesting resource or an action to be performed. A request typically consists of the following components.

- Request line
- Headers
- Bodỵ̣

1. the request line contains  

   - HTTP method(eg.get,post,put,delete)
   - URL of the resource being requested
   - HTTP version being used  

3. Headers are key-value pairs separated by a colon contain additional information about the request such as

   - user agent
   - content type
   - accepted languages
   - cookies
   - and many more

  

3. The body of the request(optional) contains data sent by the client to server such a
	  - JSON payload, raw data , text data
	  - form data (url encoded data)
	  - file uploads

  

 Not all requests have a body and its presence depends on the HTTP method and nature of request.  

#### Example 

```js
// Request line-: method , url , http version

POST /api/login HTTP/1.1

// Headers-: Host, User-Agent,Content-Type,Accept,Authorization , Content-Length

Host: www.example.com

User-Agent: Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/100.0.4896.75 Safari/537.36

Content-Type: application/json

Accept: application/json

Authorization: Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJzdWIiOiIxMjM0NTY3ODkwIiwibmFtZSI6IkpvaG4gRG9lIiwiaWF0IjoxNTE2MjM5MDIyfQ.SflKxwRJSMeKKF2QT4fwpMeJf36POk6yJV_adQssw5c

Content-Length: 44

// Request Body 

{
  "username": "john_doe",
  "password": "secretpassword"
}

```

## Types of data send in the body of the request 

- JSON Data
- URL encoded data
- raw data or text data
  


> A middle ware parses or extracts data from incoming requests. id from  different types of request bodies such as JSON,URL-encoded data ,raw data or text data

> A middleware is a function in express which may be user-defined , built-in or third party, that has access to the request and response objects of the HTTP requests(GET,POST,PUT,DELETE) and the ability to pass control to the next function(or middleware) to be executed.

  
- user defined middle wares
- built-in express middle wares
- third party middleware's

  

The middle wares has the ability to  

1. end the request response cycle
2. access to req and res objects
3. to pass control to the next function to be executed<u></u>
4. execute any code  

## Format of a user defined middleware function 

  

```js

myMiddleware(req,res,next)=>{

    //logic to handle req and res objects  

    next() // passing control to the next function

}

```

### Usage

```js

// Global use of middleware  

app.use(middlewarefunction());  

// middleware for a specific route  

app.get("/all", middlewarefunction, (req, res) => {

  console.log("Hi therew");

});

```


`app.use()` is used to use a middleware globally. This means whenever a request is received by the server from the client global middle wares will be executed first and then the control will be passed to the route handlers. Also the middle ware will be applicable for all routes

#### Examples

1. The built-in middle ware `express.json()` parses or extracts JSON data from request body and makes it available in `req.body`
2. ` express.urlencoded()` parses incoming requests with URL-encoded payloads. It extracts data from URL-encoded form submission and make it available in `req.body`
3. ` express.text()` 


## Working of cookie-parser #card

> It extracts the cookies sent by the client and makes them available in the form of an object, where each key represents the name of a cookie and its corresponding value represents the value of that cookie.
^1711016807711
- **Parsing Cookies**: When a client sends a request to the server, it may include one or more cookies in the request headers. These cookies contain information such as user authentication tokens, session identifiers, or other data that the server needs to process the request.
    
- **Middleware Execution**: When the `cookie-parser` middleware is used in an Express application, it intercepts incoming requests and parses the cookie header attached to each request.
    
- **Cookie Parsing**: The `cookie-parser` middleware parses the cookie header and extracts the individual cookies along with their values.
    
- **Making Cookies Available**: After parsing the cookie header, the `cookie-parser` middleware creates an object (`req.cookies`) containing the parsed cookies. Each key in the object represents the name of a cookie, and its corresponding value represents the value of that cookie.
    
- **Accessing Cookies**: In subsequent middleware functions or route handlers, you can access the parsed cookies from `req.cookies`. For example, if a client sends a cookie named `session_id`, you can access its value using `req.cookies.session_id`

# Error Handling refers to how Express catches and processes errors that occur both synchronously and asynchronously. Express comes with a default error handler so you don’t need to write your own to get started.

Catching Errors
It’s important to ensure that Express catches all errors that occur while running route handlers and middleware.

Errors that occur in synchronous code inside route handlers and middleware require no extra work. If synchronous code throws an error, then Express will catch and process it. For example:

app.get(‘/’, function (req, res) {

throw new Error(‘BROKEN’) // Express will catch this on its own.

})

For errors returned from asynchronous functions invoked by route handlers and middleware, you must pass them to the next() function, where Express will catch and process them. For example:

app.get(‘/’, function (req, res, next) {

fs.readFile(‘/file-does-not-exist’, function (err, data) {

if (err) {

next(err) // Pass errors to Express.

} else {

res.send(data)

}

})

})

If you pass anything to the next() function (except the string ‘route’), Express regards the current request as being an error and will skip any remaining non-error handling routing and middleware functions.

 

 

Debugging

 

Express uses the debug module internally to log information about route matches, middleware functions that are in use, application mode, and the flow of the request-response cycle. Read more here.

 

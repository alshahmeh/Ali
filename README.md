Error Handling refers to how Express catches and processes

errors that occur both synchronously and asynchronously. Express comes with a default error handler so you don’t need to write your own to get started.

 :Catching Errors

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







 : Debugging

 

Express uses the debug module internally to log information about route matches, middleware functions that are in use, application mode, and the flow of the request-response cycle. Read more here.
-------------------------------------------------------------------------------------------------------------------------------
# Code 201 Reading Notes :
|# Daily assignments|
--------------------
|1|2|3|4|5|6|7|8|9|10|11|12|13|14|15|
|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|
|here is the assignment 1|here is the assignment 2|here is the assignment 2|here is the assignment 4|here is the assignment 5|here is the assignment 6|here is the assignment 7|here is the assignment 8|here is the assignment 9|here is the assignment 10|here is the assignment 11|here is the assignment 12|here is the assignment 13|here is the assignment 14|here is the assignment 15|
-----------------------------------
# Code 102 Reading Notes :
How can I choose good texteditor:
1- It depends on personal choices
2-Some texteditor come with features not in other but all pretty similar
3-it is a software to write and manage text especially the text that you will build website
4- code completion: 
-display possible suggestions
-finish typing and possible encounter typos
-closing tags bracketsquotation marks when i opened
5-syntax highliting: 
-make the text more noticeable and easyier by color the text attributes and elements by diffrent color 
6-nice variety of them
7- the ability to choose a healthy selections of extensions available
8-write Html and css more effeciency 
9-there is shortant language called emmet that will speed up my code by writing faster-some of editors come with emmit or you can add it as extensions
10-nice series of themes: change background color series color of text and affect on text editing and some themes reduce the eye strain
11-text editor with great selections of extensions will ensure the ability to add functions  and allow you to have super power
There is a lot of text editors some of them :
1---for Mac : text edit
2---for windows : notepad
3---for linux : distribution editors one of them Gedit
When you try to using editors with your computers take some advances :
-create code in plain text without make text blood, italic ,underlined just change settings to do that
-make a folder in desktop to store your entire website  with it's documents files(with the appropriate extensios of files)
12-some editors assist you to find your mistakes 
Editors examples :
__Notepad :
-free for windows
-syntax highliting
-code ,word and function completion
-it has a zoom
- it has online community and own chatroom for questions and own searchable wiki page
-__ text wrangler: free for mac but retired
__BBedit: not free
__visual studio:
-free for windows mac linux
-has emmit shorthand for html and css
- it has syntax highliting ,themes ,extensios and code completions
__atom:
-free for windows mac linux develop by folks in github
-it has syntax highliting ,themes ,extensios
__ Brackets editor: 
-free for windows mac linux
-it develop by floks at adob photoshop
-it support html css and js
-include livepreview to update your website  once you make change automatically
__sublime text editor:
-not free 
-fast and responsive
-
- it has syntax highliting ,themes ,extensios and code completions
- --------------The diffrent between text editor and Ides are:
- text editor:edit manage texts and manage files
- Ides: integreted development environment ,it is a text editor and file manager compiler and debugger

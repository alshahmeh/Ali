The HTML tables allow web authors to arrange data like text, images, links, other tables, etc. into rows and columns of cells.

The HTML tables are created using the <table> tag in which the <tr> tag is used to create table rows and <td> tag is used to create data cells. The elements under <td> are regular and left aligned by default

Example
Live Demo
<!DOCTYPE html>
<html>

   <head>
      <title>HTML Tables</title>
   </head>
	
   <body>
      <table border = "1">
         <tr>
            <td>Row 1, Column 1</td>
            <td>Row 1, Column 2</td>
         </tr>
         
         <tr>
            <td>Row 2, Column 1</td>
            <td>Row 2, Column 2</td>
         </tr>
      </table>
      
   </body>
</html>
This will produce the following result −


Here, the border is an attribute of <table> tag and it is used to put a border across all the cells. If you do not need a border, then you can use border = "0".

Table Heading
Table heading can be defined using <th> tag. This tag will be put to replace <td> tag, which is used to represent actual data cell. Normally you will put your top row as table heading as shown below, otherwise you can use <th> element in any row. Headings, which are defined in <th> tag are centered and bold by default.

Example
Live Demo
<!DOCTYPE html>
<html>

   <head>
      <title>HTML Table Header</title>
   </head>
	
   <body>
      <table border = "1">
         <tr>
            <th>Name</th>
            <th>Salary</th>
         </tr>
         <tr>
            <td>Ramesh Raman</td>
            <td>5000</td>
         </tr>
         
         <tr>
            <td>Shabbir Hussein</td>
            <td>7000</td>
         </tr>
      </table>
   </body>
   
</html>
This will produce the following result −


Cellpadding and Cellspacing Attributes
There are two attributes called cellpadding and cellspacing which you will use to adjust the white space in your table cells. The cellspacing attribute defines space between table cells, while cellpadding represents the distance between cell borders and the content within a cell.

Example
Live Demo
<!DOCTYPE html>
<html>

   <head>
      <title>HTML Table Cellpadding</title>
   </head>
	
   <body>
      <table border = "1" cellpadding = "5" cellspacing = "5">
         <tr>
            <th>Name</th>
            <th>Salary</th>
         </tr>
         <tr>
            <td>Ramesh Raman</td>
            <td>5000</td>
         </tr>
         <tr>
            <td>Shabbir Hussein</td>
            <td>7000</td>
         </tr>
      </table>
   </body>
	
</html>
This will produce the following result −


Colspan and Rowspan Attributes
You will use colspan attribute if you want to merge two or more columns into a single column. Similar way you will use rowspan if you want to merge two or more rows.

Example
Live Demo
<!DOCTYPE html>
<html>

   <head>
      <title>HTML Table Colspan/Rowspan</title>
   </head>
	
   <body>
      <table border = "1">
         <tr>
            <th>Column 1</th>
            <th>Column 2</th>
            <th>Column 3</th>
         </tr>
         <tr>
            <td rowspan = "2">Row 1 Cell 1</td>
            <td>Row 1 Cell 2</td>
            <td>Row 1 Cell 3</td>
         </tr>
         <tr>
            <td>Row 2 Cell 2</td>
            <td>Row 2 Cell 3</td>
         </tr>
         <tr>
            <td colspan = "3">Row 3 Cell 1</td>
         </tr>
      </table>
   </body>
	
</html>
This will produce the following result −


Tables Backgrounds
You can set table background using one of the following two ways −

bgcolor attribute − You can set background color for whole table or just for one cell.

background attribute − You can set background image for whole table or just for one cell.

You can also set border color also using bordercolor attribute.

Note − The bgcolor, background, and bordercolor attributes deprecated in HTML5. Do not use these attributes.

Example
Live Demo
<!DOCTYPE html>
<html>

   <head>
      <title>HTML Table Background</title>
   </head>
	
   <body>
      <table border = "1" bordercolor = "green" bgcolor = "yellow">
         <tr>
            <th>Column 1</th>
            <th>Column 2</th>
            <th>Column 3</th>
         </tr>
         <tr>
            <td rowspan = "2">Row 1 Cell 1</td>
            <td>Row 1 Cell 2</td>
            <td>Row 1 Cell 3</td>
         </tr>
         <tr>
            <td>Row 2 Cell 2</td>
            <td>Row 2 Cell 3</td>
         </tr>
         <tr>
            <td colspan = "3">Row 3 Cell 1</td>
         </tr>
      </table>
   </body>
	
</html>
This will produce the following result −


Here is an example of using background attribute. Here we will use an image available in /images directory.

Live Demo
<!DOCTYPE html>
<html>

   <head>
      <title>HTML Table Background</title>
   </head>
	
   <body>
      <table border = "1" bordercolor = "green" background = "/images/test.png">
         <tr>
            <th>Column 1</th>
            <th>Column 2</th>
            <th>Column 3</th>
         </tr>
         <tr>
            <td rowspan = "2">Row 1 Cell 1</td>
            <td>Row 1 Cell 2</td><td>Row 1 Cell 3</td>
         </tr>
         <tr>
            <td>Row 2 Cell 2</td>
            <td>Row 2 Cell 3</td>
         </tr>
         <tr>
            <td colspan = "3">Row 3 Cell 1</td>
         </tr>
      </table>
   </body>
	
</html>
This will produce the following result. Here background image did not apply to table's header.


Table Height and Width
You can set a table width and height using width and height attributes. You can specify table width or height in terms of pixels or in terms of percentage of available screen area.

Example
Live Demo
<!DOCTYPE html>
<html>

   <head>
      <title>HTML Table Width/Height</title>
   </head>
	
   <body>
      <table border = "1" width = "400" height = "150">
         <tr>
            <td>Row 1, Column 1</td>
            <td>Row 1, Column 2</td>
         </tr>
         
         <tr>
            <td>Row 2, Column 1</td>
            <td>Row 2, Column 2</td>
         </tr>
      </table>
   </body>
	
</html>
------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
A function declaration looks like this:

function name(parameters, delimited, by, comma) {
  /* code */
}
Values passed to a function as parameters are copied to its local variables.
A function may access outer variables. But it works only from inside out. The code outside of the function doesn’t see its local variables.
A function can return a value. If it doesn’t, then its result is undefined.
To make the code clean and easy to understand, it’s recommended to use mainly local variables and parameters in the function, not outer variables.

It is always easier to understand a function which gets parameters, works with them and returns a result than a function which gets no parameters, but modifies outer variables as a side-effect.

Function naming:

A name should clearly describe what the function does. When we see a function call in the code, a good name instantly gives us an understanding what it does and returns.
A function is an action, so function names are usually verbal.
There exist many well-known function prefixes like create…, show…, get…, check… and so on. Use them to hint what a function does
Functions that are stored in object properties are called “methods”.
Methods allow objects to “act” like object.doSomething().
Methods can reference the object as this.
The value of this is defined at run-time.

When a function is declared, it may use this, but that this has no value until the function is called.
A function can be copied between objects.
When a function is called in the “method” syntax: object.method(), the value of this during the call is object.
Please note that arrow functions are special: they have no this. When this is accessed inside an arrow function, it is taken from outside.
-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

Functions are like recipes. They can execute a set of instructions on data or variables and return the result. The beauty of functions is that they are recyclable. That is, the function can be used repeatedly without having to write the same code again.

// Define a function that prints a string
function welcomeMessage() {
  console.log('Welcome to JavaScript');
}
// Call the function
welcomeMessage();
In the example above, the welcomeMessage function is used to display Welcome to JavaScript in the console. Let’s walk through this code step-by-step:

The function keyword indicates the start of a function.
The word that follows (welcomeMessage) is the function’s name.
The empty parentheses after welcomeMessage indicate that there are no parameters, or inputs, for the function.
The code between the opening ({) and closing (}) curly braces is a set of instructions. This code will only execute when the function is called.
To call a method, you need the function’s name, a pair of parentheses, and a semicolon. In this example, the function is called with welcomeMessage();.
Let’s also consider a function that receives inputs and returns outputs:

function concatName(firstName, middleName, lastName) {
  return firstName + ' ' + middleName + ' ' + lastName;
}
Let’s walk through this example step-by-step:

The concatName function is created with three parameters (inputs): firstName, middleName, and lastName. Think of these as variables that have not been set yet.
Inside of the function, the return keyword will return the concatenation of firstName, middleName, and lastName, with spaces in between each. The return keyword terminates the function it is within, and returns a value — any code inside the function that comes after the return keyword will not be evaluated (nor executed, itself).
You can save the returned string to a variable or log it to the console when you call the function.
var concatGWC = concatName('George', 'Washington', 'Carver');
In the example above, the concatName function is called with the following arguments: 'George', 'Washington', and 'Carver'. These values are saved into the variables firstName, middleName, and lastName inside of the function. The function returns a concatenation of these three strings — the concatGWC variable stores the returned concatenated string.
In this reference sheet we have used the words parameters and arguments to reference similar, but distinctly different elements of a function and function call. What’s the difference between these words?

Parameters are fields that serve as variable names inside of a function. In the example above, firstName, middleName, and lastName are parameters.
Arguments are the values passed to the function when it is called. In the example above, 'George', 'Washington', and 'Carver' are arguments.
Methods
A method, like a function, is a set of instructions that perform a task. The difference is that a method is associated with an object, while a function is not. Let’s explore some of JavaScript’s built-in methods.

var str = 'CodeCADEMY';
var str1 = str.toLowerCase();
var str2 = str.toUpperCase();
The variable str in the example above stores the string ‘CodeCADEMY’. The .toLowerCase() and .toUpperCase() methods in the example above are called on str. Let’s talk through each line:

On the second line, the .toLowerCase() method is called on the str variable, which returns the lowercase string 'codecademy'.
On the third line, the .toUpperCase() method is called on the str variable, which returns the uppercase string 'CODECADEMY'. Notice, periods are used to call a method on an object, as in str.toLowerCase();.
-----------------------------------------------------------------------------------------------------------------------------------------
Constructor :
Object()
Creates a new Object object. It is a wrapper for the given value.
Static methods :
Object.assign()
Copies the values of all enumerable own properties from one or more source objects to a target object.
Object.create()
Creates a new object with the specified prototype object and properties.
Object.defineProperty()
Adds the named property described by a given descriptor to an object.
Object.defineProperties()
Adds the named properties described by the given descriptors to an object.
Object.entries()
Returns an array containing all of the [key, value] pairs of a given object's own enumerable string properties.
Object.freeze()
Freezes an object. Other code cannot delete or change its properties.
Object.fromEntries()
Returns a new object from an iterable of [key, value] pairs. (This is the reverse of Object.entries).
Object.getOwnPropertyDescriptor()
Returns a property descriptor for a named property on an object.
Object.getOwnPropertyDescriptors()
Returns an object containing all own property descriptors for an object.
Object.getOwnPropertyNames()
Returns an array containing the names of all of the given object's own enumerable and non-enumerable properties.
Object.getOwnPropertySymbols()
Returns an array of all symbol properties found directly upon a given object.
Object.getPrototypeOf()
Returns the prototype (internal [[Prototype]] property) of the specified object.
Object.is()
Compares if two values are the same value. Equates all NaN values (which differs from both Abstract Equality Comparison and Strict Equality Comparison).
Object.isExtensible()
Determines if extending of an object is allowed.
Object.isFrozen()
Determines if an object was frozen.
Object.isSealed()
Determines if an object is sealed.
Object.keys()
Returns an array containing the names of all of the given object's own enumerable string properties.
Object.preventExtensions()
Prevents any extensions of an object.
Object.seal()
Prevents other code from deleting properties of an object.
Object.setPrototypeOf()
Sets the object's prototype (its internal [[Prototype]] property).
Object.values()
Returns an array containing the values that correspond to all of a given object's own enumerable string properties.

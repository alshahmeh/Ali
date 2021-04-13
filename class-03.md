Lists are used to group together related pieces of information so they are clearly associated with each other and easy to read. In modern web development, lists are workhorse elements, frequently used for navigation as well as general content.

Lists are good from a structural point of view as they help create a well-structured, more accessible, easy-to-maintain document. They are also useful because they provide specialized elements to which you can attach CSS styles. Finally, semantically correct lists help visitors read your web site, and they simplify maintenance when your pages need to be updated.

The three list types
There are three list types in HTML:

unordered list — used to group a set of related items in no particular order
ordered list — used to group a set of related items in a specific order
description list — used to display name/value pairs such as terms and definitions
Each list type has a specific purpose and meaning in a web page.

Unordered lists
Unordered (bulleted) lists are used when a set of items can be placed in any order. An example is a shopping list:

milk
bread
butter
coffee beans
Although the items are all part of one list, you could put the items in any order and the list would still make sense:

bread
coffee beans
milk
butter
You can use CSS to change the bullet to one of several default styles, use your own image, or even display the list without bullets — we’ll look at how to do that in the Styling lists and links article.

Unordered list markup
Unordered lists use one set of <ul></ul> tags wrapped around one or more sets of <li></li> tags:

<ul>
  <li>bread</li>
  <li>coffee beans</li>
  <li>milk</li>
  <li>butter</li>
</ul>
Ordered lists
Ordered (numbered) lists are used to display a list of items that should be in a specific order. An example would be cooking instructions:

Gather ingredients
Mix ingredients together
Place ingredients in a baking dish
Bake in oven for an hour
Remove from oven
Allow to stand for ten minutes
Serve
If the list items were moved around into a different order, the information would no longer make sense:

Gather ingredients
Bake in oven for an hour
Serve
Remove from oven
Place ingredients in a baking dish
Allow to stand for ten minutes
Mix ingredients together
Ordered lists can be displayed with several sequencing options. The default in most browsers is decimal numbers, but there are others available:

Letters
Lowercase ascii letters (a, b, c…)
Uppercase ascii letters (A, B, C…).
Lowercase classical Greek: (έ, ή, ί…)
Numbers
Decimal numbers (1, 2, 3…)
Decimal numbers with leading zeros (01, 02, 03…)
Lowercase Roman numerals (i, ii, iii…)
Uppercase Roman numerals (I, II, III…)
Traditional Georgian numbering (an, ban, gan…)
Traditional Armenian numbering (mek, yerku, yerek…)
As with unordered lists, you can use CSS to change the style of your ordered lists. See Styling lists and links for more information.

Ordered list markup
Ordered lists use one set of <ol></ol> tags wrapped around one or more sets of <li></li> tags:

<ol>
  <li>Gather ingredients</li>
  <li>Mix ingredients together</li>
  <li>Place ingredients in a baking dish</li>
  <li>Bake in oven for an hour</li>
  <li>Remove from oven</li>
  <li>Allow to stand for ten minutes</li>
  <li>Serve</li>
</ol>
Beginning ordered lists with numbers other than 1
A common requirement in ordered list usage is to get them to start with a number other than 1 (or i, or I, etc.). This is done using the start attribute, which takes a numeric value (even if you’re using CSS to change the list counters to be alphabetic or Roman). This is useful if you have a single list of items, but need to break up the list with a note or other related information. For example, we could do this with the previous example:

<ol>
  <li>Gather ingredients</li>
  <li>Mix ingredients together</li>
  <li>Place ingredients in a baking dish</li>
</ol>

<p>Before you place the ingredients in the baking dish, preheat the oven to
180 degrees centigrade/350 degrees fahrenheit in readiness for the next step.</p>

<ol start="4">
  <li>Bake in oven for an hour</li>
  <li>Remove from oven</li>
  <li>Allow to stand for ten minutes</li>
  <li>Serve</li>
</ol>
This gives the following result:

Gather ingredients
Mix ingredients together
Place ingredients in a baking dish
Before you place the ingredients in the baking dish, preheat the oven to 180 degrees centigrade/350 degrees fahrenheit in readiness for the next step.

Bake in oven for an hour
Remove from oven
Allow to stand for ten minutes
Serve
Note that this attribute was deprecated in HTML 4, so it will prevent your page from validating if you are using an HTML4 strict doctype. If you want to make use of such functionality in an HTML4 strict page, and it absolutely has to validate, you can do it using CSS Counters instead. Fortunately, however, the start attribute has been reinstated in HTML5.

Description lists
Description lists (previously called definition lists, but renamed in HTML5) associate specific names and values within a list. Examples might be items in an ingredient list and their descriptions, article authors and brief bios, or competition winners and the years in which they won. You can have as many name-value groups as you like, but there must be at least one name and at least one value in each pair.

Description lists are flexible: you can associate more than one value with a single name, or vice versa. For example, the term “coffee” can have several meanings, and you could show them one after the other:

coffee

  a beverage made from roasted, ground coffee beans
  a cup of coffee
  a social gathering at which coffee is consumed
  a medium to dark brown colour
Or, you can associate more than one name with the same value. This is useful to show variations of a term, all of which have the same meaning:

soda
pop
fizzy drink
cola

  a sweet, carbonated beverage
Description list markup
Description lists use one set of <dl></dl> tags wrapped around one or more groups of <dt></dt> (name) and <dd></dd> (value) tags. You must pair at least one <dt></dt> with at least one <dd></dd>, and the <dt></dt> should always come first in the source order.

A simple description list of single names with single values would look like this:

<dl>
  <dt>Name</dt>
  <dd>Value</dd>
  <dt>Name</dt>
  <dd>Value</dd>
  <dt>Name</dt>
  <dd>Value</dd>
</dl>
This is rendered as follows:

Name
  Value
Name
  Value
Name
  Value
In the following example, we associate more than one value with a name, and vice versa:

<dl>
  <dt>Name1</dt>
  <dd>Value that applies to Name1</dd>
  <dt>Name2</dt>
  <dt>Name3</dt>
  <dd>Value that applies to both Name2 and Name3</dd>
  <dt>Name4</dt>
  <dd>One value that applies to Name4</dd>
  <dd>Another value that applies to Name4</dd>
</dl>
That code would render like this:

Name1
  Value that applies to Name1
Name2
Name3
  Value that applies to both Name2 and Name3
Name4
  One value that applies to Name4
  Another value that applies to Name4
Choosing among list types
When trying to decide what type of list to use, ask yourself two simple questions:

Am I defining terms or associating other name/value pairs?

If yes, use a description list.
If no, don’t use a description list.
Is the order of the list items important?

If yes, use an ordered list.
If no, use an unordered list.
HTML list advantages
Flexibility: If you have to change the order of the list items in an ordered list, you simply move around the list item elements; when the browser renders the list, it will be properly ordered.
Styling: Using an HTML list allows you to style the list properly using CSS. The list item tags <li> are different from the other tags in your document, so you can specifically target CSS rules to them.
Semantics: HTML lists give the content the proper semantic structure. This has important benefits, such as allowing screen readers to tell users with visual impairments that they are reading a list, rather than just reading out a confusing jumble of text and numbers.
To put it another way, don’t code list items using regular text tags. Using text instead of a list makes more work for you and can create problems for your document’s readers. So if your document needs a list, you should use the correct HTML list format.

Nesting lists
An individual list item can contain another entire list, called a nested list. It is useful for things like tables of contents that contain sub-sections:

1. Chapter One
    a. Section One
    b. Section Two
    c. Section Three
2. Chapter Two
3. Chapter Three
To reflect that in the code, the entire nested list is contained inside the first list item. The code looks like this:

<ol>
  <li>Chapter One
    <ol style="list-style-type: lower-alpha;">
      <li>Section One</li>
      <li>Section Two </li>
      <li>Section Three </li>
    </ol>
  </li>
  <li>Chapter Two</li>
  <li>Chapter Three  </li>
</ol>
Note that we have used the list-style-type: lower-alpha CSS property to sequence the nested list with lower-case letters instead of decimal numbers.

Nested lists are quite useful, and often form the basis for navigation menus, as they are a good way to define the hierarchical structure of the web site. They are also very flexible, as either ordered or unordered lists can be nested inside either ordered or unordered list items. For an example of nesting unordered lists within an ordered list, see “Choosing among list types” above.

Theoretically you can nest lists to any level you like, although in practice it can become confusing to nest lists too deeply. For very large lists, you may be better off splitting the content up into several lists with headings instead, or even splitting it up into separate pages. A good rule of thumb is, don’t nest lists deeper than three levels.

---------------------------------------------------------------------------------------------------------------------------------------------------
![image](https://user-images.githubusercontent.com/81554444/114594982-8a0bf900-9c96-11eb-86fc-1cdb8b9d9b8c.png)
 Box dimensions
Each box has a content area (e.g., text, an image, etc.) and optional surrounding padding, border, and margin areas; the size of each area is specified by properties defined below. The following diagram shows how these areas relate and the terminology used to refer to pieces of margin, border, and padding:

The margin, border, and padding can be broken down into top, right, bottom, and left segments (e.g., in the diagram, "LM" for left margin, "RP" for right padding, "TB" for top border, etc.).

The perimeter of each of the four areas (content, padding, border, and margin) is called an "edge", so each box has four edges:

content edge or inner edge
The content edge surrounds the rectangle given by the width and height of the box, which often depend on the element's rendered content. The four content edges define the box's content box.
padding edge
The padding edge surrounds the box padding. If the padding has 0 width, the padding edge is the same as the content edge. The four padding edges define the box's padding box.
border edge
The border edge surrounds the box's border. If the border has 0 width, the border edge is the same as the padding edge. The four border edges define the box's border box.
margin edge or outer edge
The margin edge surrounds the box margin. If the margin has 0 width, the margin edge is the same as the border edge. The four margin edges define the box's margin box.
Each edge may be broken down into a top, right, bottom, and left edge.

The dimensions of the content area of a box — the content width and content height — depend on several factors: whether the element generating the box has the 'width' or 'height' property set, whether the box contains text or other boxes, whether the box is a table, etc. Box widths and heights are discussed in the chapter on visual formatting model details.

The background style of the content, padding, and border areas of a box is specified by the 'background' property of the generating element. Margin backgrounds are always transparent.

8.2 Examp
9.------------------------------------------------------------------------------------------------------------------------------------------------------------------------
10.The for Loop
The for loop lets JavaScript executes the statements repeatedly until it meets a certain condition. The syntax is:

for (initial expression; condition expression; loop expression)
{ Statements}Example 8.1
<html>
<head>
<title>For Loop</title>
</head>
<body>
<script language='javascript'>
var sum=0
for (n=0; n<11; n++)
 { sum+=n   }
 document.write("sum="+sum)
</script>
</body>
In the above example, the initial expression is n=0, the condition expression is n<11 and the loop expression is n++. It means the loop will stop only when n is more than 11. The statement sum+=n means n is added to the sum in every repetition. Finally, the browser will display the final value of the sum, which is 55 in this example.The While Loop
The while statement allows us to control the number of times a procedure is performed. It is important to make that the repetition is not endless. The algorithm is illustrated in example 8.3. The program will produce a pop-up dialog box 8 times prompting the user to enter the marks 8 times, then it will add up the marks and show the average mark.

Example 8.3
<html>
<head>
<meta http-equiv="Content-Language" content="zh-cn">
<meta http-equiv="Content-Type" content="text/html; charset=gb2312">
<title>Sample JavaScript using While</title>
<script>

var sum,
mark1,
mark2,
counter,
avg;

sum=0;
counter=1;

while(counter<=8) {

mark1=window.prompt("Enter your mark","0");
mark2=parseInt(mark1);
sum=sum+mark2;
counter=counter+1;
}
avg=sum/8;
document.writeln("<H2> Average mark is "+avg+"</H2>");

</script>
</head>

<body>

<h2 align="center"><font face="Arial">Sample JavaScript using While</font></h2>

</body>

</html>
Javascript Decision Making
Decision Making statements are if, else, elseif and switch these statements are used in making decisions.



if..else statements
if..else statements is used where you want to execute a set of code when a condition is true and another if the condition is not true

Syntax


if (condition)
{
  code to be executed if condition is true
}
else
{
  code to be executed if condition is false
}

Example of if..else

var a=10;
if (a==10)
{
  echo "Yes the value is 10"; 
}
else
{
  echo "No the value is not 10"; 
}

elseif statements
elseif statements is used where you want to execute a some code if one of several conditions are true use the elseif statement


Syntax


if (condition)
{
  code to be executed if condition is true
}
elseif (condition)
{
  code to be executed if condition is true;
}
else
{
  code to be executed if condition is false
}

Example of elseif

var a=10;
if (a==20)
{
  echo "Yes the value is 20"; 
}
elseif(a==10)
{
  echo "Yes the value is 10"; 
}
else
{
  echo "No you are wrong"; 
}

switch statements
switch statements is used where you want to execute one block of code out of many.


Syntax


switch (value)
{
case value1:
  code to be executed if value = value1;
  break;  

case value2:
  code to be executed if value = value2;
  break;

default:
  code to be executed
  if value is different 
  from both value1 and value2;
}

Example of switch

var a=10;
switch ( a )
{
case 10:
  code to be executed if var a=10;
  break;  

case 20:
  code to be executed if var a=20;
  break;

default:
  code to be executed
  if value is different 
  from both value1 and value2;

}

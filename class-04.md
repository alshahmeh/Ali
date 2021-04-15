 
Images are very important to beautify as well as to depict many complex concepts in simple way on your web page. This tutorial will take you through simple steps to use images in your web pages.

Insert Image
You can insert any image in your web page by using <img> tag. Following is the simple syntax to use this tag.

<img src = "Image URL" ... attributes-list/>
The <img> tag is an empty tag, which means that, it can contain only list of attributes and it has no closing tag.

Example
To try following example, let's keep our HTML file test.htm and image file test.png in the same directory −

Live Demo
<!DOCTYPE html>
<html>

   <head>
      <title>Using Image in Webpage</title>
   </head>
	
   <body>
      <p>Simple Image Insert</p>
      <img src = "/html/images/test.png" alt = "Test Image" />
   </body>
	
</html>
This will produce the following result −


You can use PNG, JPEG or GIF image file based on your comfort but make sure you specify correct image file name in src attribute. Image name is always case sensitive.

The alt attribute is a mandatory attribute which specifies an alternate text for an image, if the image cannot be displayed.

Set Image Location
Usually we keep all the images in a separate directory. So let's keep HTML file test.htm in our home directory and create a subdirectory images inside the home directory where we will keep our image test.png.

Example
Assuming our image location is "image/test.png", try the following example −

Live Demo
<!DOCTYPE html>
<html>

   <head>
      <title>Using Image in Webpage</title>
   </head>
	
   <body>
      <p>Simple Image Insert</p>
      <img src = "/html/images/test.png" alt = "Test Image" />
   </body>
	
</html>
This will produce the following result −


Set Image Width/Height
You can set image width and height based on your requirement using width and height attributes. You can specify width and height of the image in terms of either pixels or percentage of its actual size.

Example
Live Demo
<!DOCTYPE html>
<html>

   <head>
      <title>Set Image Width and Height</title>
   </head>
	
   <body>
      <p>Setting image width and height</p>
      <img src = "/html/images/test.png" alt = "Test Image" width = "150" height = "100"/>
   </body>
	
</html>
This will produce the following result −


Set Image Border
By default, image will have a border around it, you can specify border thickness in terms of pixels using border attribute. A thickness of 0 means, no border around the picture.

Example
Live Demo
<!DOCTYPE html>
<html>

   <head>
      <title>Set Image Border</title>
   </head>
	
   <body>
      <p>Setting image Border</p>
      <img src = "/html/images/test.png" alt = "Test Image" border = "3"/>
   </body>
	
</html>
This will produce the following result −


Set Image Alignment
By default, image will align at the left side of the page, but you can use align attribute to set it in the center or right.

Example
Live Demo
<!DOCTYPE html>
<html>

   <head>
      <title>Set Image Alignment</title>
   </head>
	
   <body>
      <p>Setting image Alignment</p>
      <img src = "/html/images/test.png" alt = "Test Image" border = "3" align = "right"/>
   </body>
	
</html>
This will produce the following result −


--------------------------------------------------------------------------------------------------------------------------------------
HTML Color Codes Theory
So you are wondering "Does this weird combination of letters and numbers have any meaning?" Well the answer is "Yes" and this is how it goes:)

HTML Codes format:
Each HTML code contains symbol "#" and 6 letters or numbers. These numbers are in hexadecimal numeral system. For example "FF" in hexadecimal represents number 255 in Decimal.

Meaning of symbols:
The first two symbols in HTML color code represents the intensity of red color. 00 is the least and FF is the most intense. The third and fourth represents intensity of green and fifth and sixth represents the intensity of blue. So with combining the intensity of red, green and blue we can mix almost any color that our heart desire;)

Examples:
#FF0000 - With this HTML code we tell browser to show maximum of red and no green and no blue. The result is of course pure red color:     

#00FF00 - This HTML code shows just green and no red and blue. The result is:     

#0000FF - This HTML code shows just blue and no red and green. The result is:     

#FFFF00 - Combination of red and green color gives us yellow:     

#CCEEFF - Take some red a bit more of green and maximum of blue to get color of sky:     

------------------------------------------------------------------------------------------------------------------------------------------------------
The p tag
This tag defines a paragraph of text.

<p>Some text</p>
It’s a block element.

Inside it, we can add any inline element we like, like span or a.

We cannot add block elements.

We cannot nest p elements one into another.

By default browsers style a paragraph with a margin on top and at the bottom. 16px in Chrome, but the exact value might vary between browsers.

This causes two consecutive paragraphs to be spaced, replicating what we think of a “paragraph” in printed text.

The span tag
This is an inline tag that can be used to create a section in a paragraph that can be targeted using CSS:

<p>A part of the text <span>and here another part</span></p>
The br tag
This tag represents a line break. It’s an inline element, and does not need a closing tag.

We use it to create a new line inside a p tag, without creating a new paragraph.

And compared to creating a new paragraph, it does not add additional spacing.

<p>Some text<br>A new line</p>
The heading tags
HTML provides us 6 heading tags. From most important to least important, we have h1, h2, h3, h4, h5, h6.

Typically a page will have one h1 element, which is the page title. Then you might have one or more h2 elements depending on the page content.

Headings, especially the heading organization, are also essential for SEO, and search engines use them in various ways.

The browser by default will render the h1 tag bigger, and will make the elements size smaller as the number near h increases:

Headings

All headings are block elements. They cannot contain other elements, just text.

The strong tag
This tag is used to mark the text inside it as strong. This is pretty important, it’s not a visual hint, but a semantic hint. Depending on the medium used, its interpretation will vary.

Browsers by default make the text in this tag bold.

The em tag
This tag is used to mark the text inside it as emphasized. Like with strong, it’s not a visual hint but a semantic hint.

Browsers by default make the text in this italic.

Quotes
The blockquote HTML tag is useful to insert citations in the text.

Browsers by default apply a margin to the blockquote element. Chrome applies a 40px left and right margin, and a 10px top and bottom margin.

The q HTML tag is used for inline quotes.

Horizontal line
Not really based on text, but the hr tag is often used inside a page. It means horizontal rule, and it adds an horizontal line in the page.

Useful to separate sections in the page.

Code blocks
The code tag is especially useful to show code, because browsers give it a monospaced font.

That’s typically the only thing that browsers do. This is the CSS applied by Chrome:

code {
    font-family: monospace;
}
This tag is typically wrapped in a pre tag, because the code element ignores whitespace and line breaks. Like the p tag.

Chrome gives pre this default styling:

pre {
    display: block;
    font-family: monospace;
    white-space: pre;
    margin: 1em 0px;
}
which prevents white space collapsing and makes it a block element.

Lists
We have 3 types of lists:

unordered lists
ordered lists
definition lists
Unordered lists are created using the ul tag. Each item in the list is created with the li tag:

<ul>
	<li>First</li>
	<li>Second</li>
</ul>
Ordered lists are similar, just made with the ol tag:

<ol>
	<li>First</li>
	<li>Second</li>
</ol>
The difference between the two is that ordered lists have a number before each item:

Lists

Definition lists are a bit different. You have a term, and its definition:

<dl>
	<dt>Flavio</dt>
	<dd>The name</dd>
	<dt>Copes</dt>
	<dd>The surname</dd>
</dl>
This is how browsers typically render them:

Definition list

I must say you rarely see them in the wild, for sure not much as ul and ol, but sometimes they might be useful.

Other text tags
There is a number of tags with presentational purposes:

the mark tag
the ins tag
the del tag
the sup tag
the sub tag
the small tag
the i tag
the b tag
This is an example of the visual rendering of them which is applied by default by browsers:

Various tags

You might wonder, how is b different than strong? And how i is different than em?

The difference lies in the semantic meaning. While b and i are a direct hint at the browser to make a piece of text bold or italic, strong and em give the text a special meaning, and it’s up to the browser to give the styling. Which happens to be exactly the same as b and i, by default. Although you can change that using CSS.

There are a number of other, less used tags related to text. I just mentioned the ones that I see used the most.

---------------------------------------------------------------------------------------------------------------------------------------------------------------
You should be aware of a few key factors...

First, there are two types of compression: Lossless and Lossy.

Lossless means that the image is made smaller, but at no detriment to the quality.
Lossy means the image is made (even) smaller, but at a detriment to the quality. If you saved an image in a Lossy format over and over, the image quality would get progressively worse and worse.
There are also different colour depths (palettes): Indexed color and Direct color.

Indexed means that the image can only store a limited number of colours (usually 256), controlled by the author, in something called a Color Map
Direct means that you can store many thousands of colours that have not been directly chosen by the author
BMP - Lossless / Indexed and Direct

This is an old format. It is Lossless (no image data is lost on save) but there's also little to no compression at all, meaning saving as BMP results in VERY large file sizes. It can have palettes of both Indexed and Direct, but that's a small consolation. The file sizes are so unnecessarily large that nobody ever really uses this format.

Good for: Nothing really. There isn't anything BMP excels at, or isn't done better by other formats.

BMP vs GIF

GIF - Lossless / Indexed only

GIF uses lossless compression, meaning that you can save the image over and over and never lose any data. The file sizes are much smaller than BMP, because good compression is actually used, but it can only store an Indexed palette. This means that for most use cases, there can only be a maximum of 256 different colours in the file. That sounds like quite a small amount, and it is.

GIF images can also be animated and have transparency.

Good for: Logos, line drawings, and other simple images that need to be small. Only really used for websites.

GIF vs JPEG

JPEG - Lossy / Direct

JPEGs images were designed to make detailed photographic images as small as possible by removing information that the human eye won't notice. As a result it's a Lossy format, and saving the same file over and over will result in more data being lost over time. It has a palette of thousands of colours and so is great for photographs, but the lossy compression means it's bad for logos and line drawings: Not only will they look fuzzy, but such images will also have a larger file-size compared to GIFs!
-----------------------------
PNG is a newer format, and PNG-8 (the indexed version of PNG) is really a good replacement for GIFs. Sadly, however, it has a few drawbacks: Firstly it cannot support animation like GIF can (well it can, but only Firefox seems to support it, unlike GIF animation which is supported by every browser). Secondly it has some support issues with older browsers like IE6. Thirdly, important software like Photoshop have very poor implementation of the format. (Damn you, Adobe!) PNG-8 can only store 256 colours, like GIFs.

Good for: The main thing that PNG-8 does better than GIFs is having support for Alpha Transparency.
---------------------------
GIF uses lossless compression, meaning that you can save the image over and over and never lose any data. The file sizes are much smaller than BMP, because good compression is actually used, but it can only store an Indexed palette. This means that for most use cases, there can only be a maximum of 256 different colours in the file. That sounds like quite a small amount, and it is.

GIF images can also be animated and have transparency.

Good for: Logos, line drawings, and other simple images that need to be small. Only really used for websites.

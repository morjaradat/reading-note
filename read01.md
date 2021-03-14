# Introdution 
## About this book
-  This book talk about how to make web page  with HTML and CSS 
## How the web works
- The web works by reading html code
When you visit a website, the web server
hosting that site could be anywhere in the
world. In order for you to find the location of
the web server, your browser will first connect
to a Domain Name System (DNS) server. 

# Structure 
- The major component HTML  page  :
1. doctype 
2. html tag
3. head tag
4. body tag

- HTML pages are text documents.
- HTML uses tags (characters that sit inside angled
brackets) to give the information they surround special
meaning.
- Tags are often referred to as elements.
- Tags usually come in pairs. The opening tag denotes
the start of a piece of content; the closing tag denotes
the end.
- Opening tags can carry attributes, which tell us more
about the content of that element.
- Attributes require a name and a value.
- To learn HTML you need to know what tags are
available for you to use, what they do, and where they
can go.
- HTML uses elements to describe the structure of pages.  
- We can Look at Other sites are Built by View source .  

# Extra Markup 
##  DOCTYPEs :
- DOCTYPE declaration to tell a
browser which version of HTML
the page is using
## comments  in HTML
- If we want to add a comment
to your code that will not be
visible in the user's browser .
## ID Attribute 
- Every HTML element can carry
the id attribute. 
- It is used to
uniquely identify that element
from other elements on the
page. 
## Class Attribute
- Every HTML element can
also carry a class attribute.
- Sometimes, rather than uniquely
identifying one element within
a document, you will want a
way to identify several elements
 ## Block ELEMENT 
 - Some elements will always
appear to start on a new line in
the browser window. These are
known as block level elements. 
- Examples of block elements are
h1, p, ul, and li TAGS .
## Inline ELEMENT 
- Some elements will always
appear to continue on the
same line as their neighbouring
elements. These are known as
inline elements.
- Examples of inline elements are
a, b, em, and img tags .
## Grouping Text &Elements In a Block 
- The div element allows you to
group a set of elements together
in one block-level box. 
## Grouping Text & Elements Inline 
-  The span element acts like
an inline equivalent of the div
element. It is used to either:
1. Contain a section of text
where there is no other suitable
element to differentiate it from
its surrounding text .
2. Contain a number of inline
elements
The most common reason why
people use span elements
is so that they can control the
appearance of the content of
these elements using CSS. 
## IFrames 
- An iframe is like a little window
that has been cut into your
page — and in that window you
can see another page. The term
iframe is an abbreviation of inline
frame. 
- One common use of iframes
(that you may have seen on
various websites) is to embed
a Google Map into a page .
### src
- The src attribute specifies the
URL of the page to show in the
frame.
### height
- The height attribute specifies
the height of the iframe in pixels.
### width
- The width attribute specifies
the width of the iframe in pixels.
### scrolling
- The scrolling attribute will
not be supported in HTML5. In
HTML 4 and XHTML, it indicates
whether the iframe should
have scrollbars or not .
 ### frameborder 
 - The frameborder attribute will
not be supported in HTML5. In
HTML 4 and XHTML, it indicates
whether the frame should have
a border or not. A value of 0
indicates that no border should
be shown. A value of 1 indicates
that a border should be shown .
 ### seamless 
 - In HTML5, a new attribute
called seamless can be applied
to an iframe where scrollbars
are not desired. The seamless
attribute (like some other new
HTML5 attributes) does not
need a value, but you will often
see authors give it a value of
seamless. Older browsers
do not support the seamless
attribute.
## meta ELEMENT 
- The meta element lives
inside the head element and
contains information about that
web page. 
- It is not visible to users but
fulfills a number of purposes
such as telling search engines
about your page, who created
it, and whether or not it is time
sensitive.
- The meta element is an empty
element so it does not have a
closing tag. 
-  It uses attributes to
carry the information. 
- The most common attributes
are the name and content
attributes, which tend to be
used together.
### description 
- This contains a description
of the page. 
- This description
is commonly used by search
engines to understand what the
page is about and should be a
maximum of 155 characters.
### keywords
- This contains a list of commaseparated
words that a user
might search on to find the page.
In practice, this no longer has
any noticeable effect on how
search engines index your site .
### robots 
- This indicates whether search
engines should add this page
to their search results or not.
- A value of noindex can be used if
this page should not be added .
 ### author
 - This defines the author of the
web page.
### pragma 
- This prevents the browser from
caching the page. (That is,
storing it locally to save time
downloading it on subsequent
visits.)
### expires
- Because browsers often cache
the content of a page, the
expires option can be used
to indicate when the page
should expire (and no longer be
cached). 
- Note that the date must
be specified in the format shown .
## Escape Characters 
- Therefore, if you want these
characters to appear on your
page you need to use what are
termed "escape" characters
(also known as escape codes or
entity references).
-  For example,to write a left angled bracket,
you can use either &lt; or
&#60;. For an ampersand, you
can use either &amp; or &#38;.
- There are also special codes
that can be used to show
symbols such as copyright and
trademark, currency symbols,
mathematical characters, and
some punctuation marks. For
example, if you want to include a
copyright symbol on a web page
you can use either &copy; or
&#169;.
- When using escape characters,
it is important to check the
page in your browser to ensure
that the correct symbol shows
up. This is because some fonts
do not support all of these
characters and you might
therefore need to specify
a different font for these
characters in your CSS code.
## Summary
* DOCTYPES tell browsers which version of HTML you
are using.
* You can add comments to your code between the markers..
* The id and class attributes allow you to identify
particular elements.

* The div and span elements allow you to group
block-level and inline elements together.
* iframes cut windows into your web pages through
which other pages can be displayed.
* The meta tag allows you to supply all kinds of
information about your web page.
* Escape characters are used to include special
characters in your pages such as <, >, and ©.  

# HTML5 Layout
## Traditional HTML Layouts 
- For a long time, web page authors used div elements to group
together related elements on the page (such as the elements that form a
header, an article, footer or sidebar). 
- Authors used class or id attributes
to indicate the role of the div element in the structure of the page.
## New Html5 Layout Elements
- HTML5 introduces a new set of elements that allow you to divide up the
parts of a page. 
- The names of these elements indicate the kind of content
you will find in them. 
- They are still subject to change, but that has not
stopped many web page authors using them already.
### Headers & Footers
- The header and footer
elements can be used for:

1. The main header or footer
that appears at the top or
bottom of every page on the
site.
2. A header or footer for an
individual article or
section within the page .

### Navigation
- The nav element is used to
contain the major navigational
blocks on the site such as the
primary site navigation.
### ArticlesThe <article> element acts as
- a container for any section of a
page that could stand alone and
potentially be syndicated.
- This could be an individual
article or blog entry, a comment
or forum post, or any other
independent piece of content .

### Aside 
- The aside element has two
purposes, depending on whether
it is inside an article
element or not.
- When the aside element
is used inside an article
element, it should contain
information that is related to the
article but not essential to its
overall meaning.
 ### Sections
 - The section element groups
related content together, and
typically each section would
have its own heading.
### Heading Groups
- The purpose of the hgroup
element is to group together a
set of one or more h1 through
h6 elements so that they are
treated as one single heading.
### Figures 
- You already met the figure
element in Chapter 5 when we
looked at images. It can be used
to contain any content that is
referenced from the main flow of
an article (not just images).
### Sectioning Elements
- It may seem strange to follow
these new elements by revisiting
the div element again. 
### Linking Around Block-Level Elements
- HTML5 allows web page authors
to place an a element around
a block level element that
contains child elements. This
allows you to turn an entire block
into a link.
### Helping Older Browsers Understand
- Older browsers that do not
know the new HTML5 elements
will automatically treat them as
inline elements. Therefore, to
help older browsers, you should
include the line of CSS on the
left which states which new
elements should be rendered as
block-level elements.
## Summary
- The new HTML5 elements indicate the purpose of
different parts of a web page and help to describe
its structure.
- The new elements provide clearer code (compared
with using multiple div elements).
- Older browsers that do not understand HTML5
elements need to be told which elements are
block-level elements.
- To make HTML5 elements work in Internet Explorer 8
(and older versions of IE), extra JavaScript is needed,
which is available free from Google. 
# Process & Design 
- This section discusses a process that
you can use when you are creating a new
website.
## Who is the Site For? 
- Every website should be designed for the
target audience—not just for yourself or the
site owner. It is therefore very important to
understand who your target audience is .
- Invent some fictional visitors from your typical
target audience. They will become your friends.
They can influence design decisions from color
palettes to level of detail in descriptions.
## Why People Visit YOUR Website
1. The first attempts to discover
the underlying motivations for
why visitors come to the site.
2. The second examines the
specific goals of the visitors.
These are the triggers making
## What Your Visitors are Trying to Achieve 
- It is unlikely that you will be able to list every
reason why someone visits your site but you
are looking for key tasks and motivations. This
information can help guide your site designs.
## What Information Your Visitors Need 
- You may want to offer additional
supporting information that you
think they might find helpful.
- Look at each of the reasons why
people will be visiting your site
and determine what they need to
achieve their goals.
- You can prioritize levels of
information from key points
down to non-essential or
background information.
## How Of ten People Will Visit Your Site 
- A website about fashion trends
will need to change a lot more
frequently than one that is
promoting a service that people
do not buy regularly (such as
domestic plumbing or double
glazing).
- Once a site has been built, it can
take a lot of time and resources
to update it frequently. 
## Site Maps 
- The aim is to create a diagram
of the pages that will be used
to structure the site. This is
known as a site map and it will
show how those pages can be
grouped.
- To help you decide what
information should go on each
page, you can use a technique
called card sorting.

## WireFrames
- A wireframe is a simple sketch of the key
information that needs to go on each page of a
site. It shows the hierarchy of the information
and how much space it might require
## Getting your message across using design 
- The primary aim of any kind of visual design
is to communicate. Organizing and prioritizing
information on a page helps users understand
its importance and what order to read it in.
## Visual hierarchy
- Most web users do not read entire pages. Rather, they skim to find
information.
-  You can use contrast to create a visual hierarchy that gets
across your key message and helps users find what they are looking for. 
### SIZE
Larger elements will grab users'
attention first. For this reason it
is a good idea to make headings
and key points relatively large.
### COLOR
Foreground and background
color can draw attention to key
messages. Brighter sections tend
to draw users' attention first.
### Style
An element may be the same
size and color as surrounding
content but have a different style
applied to it to make it stand out.
## grouping and Similarity
- When making sense of a design, we tend to organize visual elements
into groups. Grouping related pieces of information together can make a
design easier to comprehend. 
### Proximity
When several items are
placed close together, they are
perceived as more related than
items that are placed further
apart. (You can also nest groups
of information within larger
groups of information.)
### Closure
When faced with a complicated
arrangement of items, we
will often look for a single or
recognisable pattern or form.
A real or imaginary box can be
formed around elements due to
their proximity and alignment.
### Continuance
When elements are placed in
a line or a curve then they are
perceived to be more related
than those that are not following
the same direction. This can be
used to direct a reader from one
part of a page to the next.
### White Sp ace
Placing related items closer
together and leaving a bigger
gap between unrelated items 
### color
A background color placed
behind related items to
emphasize their connection. 
### Borders
A line can be drawn around the
border of the group or between it
and its neighbors.
## Designing Navigation 
- Site navigation not only helps people find where they want to go, but also
helps them understand what your site is about and how it is organized.
Good navigation tends to follow these principles...
### Concise
- Ideally, the navigation should
be quick and easy to read. It is
a good idea to try to limit the
number of options in a menu to
no more than eight links. These
can link to section homepages
which in turn link to other pages.
### Clear
- Users should be able to predict
the kind of information that
they will find on the page
before clicking on the link.
Where possible, choose single
descriptive words for each link
rather than phrases.
### Selective
- The primary navigation should
only reflect the sections or
content of the site. Functions
like logins and search, and legal
information like terms and
conditions and so on are best
placed elsewhere on the page
## Summary 
- It's important to understand who your target audience
is, why they would come to your site, what information
they want to find and when they are likely to return.
- Site maps allow you to plan the structure of a site. 
- Wireframes allow you to organize the information that
will need to go on each page.
- Design is about communication. Visual hierarchy helps
visitors understand what you are trying to tell them.
- You can differentiate between pieces of information
using size, color, and style. 
- You can use grouping and similarity to help simplify
the information you present. 

# The ABC of Programming 
## what script  mean ?
 A script is a series of instructions that a
computer can follow to achieve a goal .
 how to wriite a script 
## To write a script,
 we need to first state your goal and then list the
tasks that need to be completed in
order to achieve it. 
* simply by three steps : *
1. DEFINE THE GOAL.
2. DESIGN THE SCRIPT
3. CODE EACH STEP
 
## EXPRESSIONS 
An expression evaluates into (results in) a single value. Broadly speaking there are two types of expressions :
1. EXPRESSIONS THAT JUST ASSIGN A VALUE TO A VARIABLE 
- In order for a variable to be useful, it needs to be given a value ** var color = 'beige'; **

2. EXPRESSIONS THAT USE TWO OR MORE VALUES TO RETURN A SINGLE VALUE 

- You can perform operations on any number of
individual values (see next page) to determine a
single value. For example:
** var area = 3 * 2; **
 
 ## OPERATORS
- Expressions rely on things called operators; they allow programmers to
create a single value from one or more values.

## They are many operators  like :
1. ASSIGNMENT OPERATORS
Assign a value to a 
2. ARITHMETIC OPERATORS
Perform basic math
3. STRING OPERATORS
Combine two strings
4. COMPARISON OPERATORS
Compare two values and return true or fa1se
5. LOGICAL OPERATORS
Combine expressions and return true or fa1se 

### JavaScript contains the following mathematical operators, which you can use with numbers  like : 
- ADDITION + , - SUBTRACTION  , DIVISION / , MULTIPLICATION * , INCREMENT + + ,  DECREMENT -- and  MODULUS %  
 
 ### STRING OPERATOR 
 There is just one string operator: the+ symbol ; It is used to join the strings on either side of it like :
** var firstName = 'Ivy ' ; **
 ** var lastName = ' Stone' ; **
** var ful l Name = f irstName + l astName; ** 
 
 - we can use  mixing number and  strings together  like : 
 ** var cost l = '7'; 
 var cost2 = '9 ' ; 
var total = costl + cost2 ; ** 

## Function 
Functions let you group a series of statements together to perform a
specific task.
- To create a function  we give it a name and then write the statments needed to achieve its task inside the curly braces . 
- We can call  the function by function name (); 
- some function need specific information to perform its task  like : 
function getare (weight , height) 
# Web Notes
## HTML 
***

 HTML ( HyperText Markup Language )is the basic building block of  the web. It defines  the meaning and structure of we content. ==Css== (cassading stylesheet) is use to describe the apperance /presentation  or Functionality and/Behavior(javascript)
 
 HTML uses "markup" to annotate text, images and other content for web display 
 
markup has special "elements" such as
  
 what is a elements
  an element is  everything from the start tag to the  end tag and the content in between
  
 	<head>,<title> <body><nav><img><footer><article><section> etc, 	many others.-->

	 <p class =""> hello world </p>
 	tags 
 	"< >" "</>" 
 
 what is an attribute and it vaule
  	
 attributes contain extra information about
 that you can later grab in css and javascript
 
   	<p class='editor notes'> I love jelly</p>
   	     ^---attribute---^
   	     
  1  A space between it and the element name (or the previous attribute, if the element already has one or more attributes).

 2 The attribute name followed by an equal sign.
 
 3 The attribute value wrapped by opening and   closing quotation marks.
 
  you can nest elements
  example:
  
 	 <p>My cat is <strong>very</strong> grumpy.</p>
result:
 <p>My cat is <strong>very</strong> grumpy.</p>
 
 
Some elements have no content and are called empty elements. Take the <img> element that we already have in our HTML page:

	<img src="images/firefox-icon.png" alt="My test image">

<img src="images/firefox-icon.png" alt="My test image">

This contains two attributes, but there is no closing </img> tag and no inner content. This is because an image element doesn't wrap content to affect it. Its purpose is to embed an image in the HTML page in the place it appears.


1. <!DOCTYPE html> — the doctype. It is required preamble. In the mists of time, when HTML was young (around 1991/92), doctypes were meant to act as links to a set of rules that the HTML page had to follow to be considered good HTML, which could mean automatic error checking and other useful things. However these days, they don't do much, and are basically just needed to make sure your document behaves correctly. That's all you need to know for now.

1.` <html></html> `— the <html> element. This element wraps all the content on the entire page and is sometimes known as the root element.

1.  `<head></head> `— the  `<head> `element. This element acts as a container for all the stuff you want to include on the HTML page that isn't the content you are showing to your page's viewers. This includes things like keywords and a page description that you want to appear in search results, CSS to style our content, character set declarations and more.

1. `<meta charset="utf-8">` — This element sets the character set your document should use to UTF-8 which includes most characters from the vast majority of written languages. Essentially, it can now handle any textual content you might put on it. There is no reason not to set this and it can help avoid some problems later on.

1. `<title></title>` — the `<title>` element. This sets the title of your page, which is the title that appears in the browser tab the page is loaded in. It is also used to describe the page when you bookmark/favourite it.

1. ` <body></body>` — the `<body>` element. This contains all the content that you want to show to web users when they visit your page, whether that's text, images, videos, games, playable audio tracks or whatever else.

list  contains two elements 
and two different list styles
 
 unorder list order list
 
 	<ul>
 		<li>technology</li>
 		<li>thinkers</li>
 		<li>builder</li>
 	<ul> 
 	
 	order list 
 		good for reicpe and instruction 
 		<ol>
 			<li> technology</li>
 			<li>thinkers</li>
 			<li>builder</li>
 		</ol>
 		
 		
 links make the web,
 here how to make a web link
 
 	<a>Mainfesto</a>
 	<a href ="https://www.mozilla.org/en-US/about/manifesto/" >some thing magical</a>

<a href ="https://www.mozilla.org/en-US/about/manifesto/" >some thing magical the mozilla manifesto</a>

comment in html  

	<!-- no thing will show here leave comments -->

to move thought  throught folders 
you got  / to go forward in subfolders
 and  . to go back 
 
 	<link rel="stylesheet" type="text/css" href="../css/style.css">
 	
 

## CSS
 
 CSS(cascading Style sheets
 CSS is not  mark up language it's
 a style sheet language
 
  you can apply style to selected elements
  to html document 
  
  example 
  
	 p{
	   color: red;
	  }

 save this in a new file  call it style.css 
 to link the css
  <link href="styles/styles.css" rel="stylesheet">
  
  p is a selector
  color is property end with :
  red is  property value  ends with  ;
  
##### selector 
  the html element name  to be style 
  to me its the tag that begin styled
   you can also called class  or and ids
   
   can select multipe types of elements
	
	p,li,h1{
		 color : red;
		 width:500px;
		 border: 1px solid black;
	}   
allowed one element per ID and of course one ID per element
 
 	#my-id{
	 	color : red;
		 width:500px;
		 border: 1px solid black;
		} 
	
	<p id="my-id"></p>

class selector 

The class selector consists of a dot, '.', followed by a class name. A class name is any value, without spaces, placed within an HTML class attribute. It is up to you to choose a name for the class. It is also noteworthy that multiple elements in a document can have the same class value, and a single element can have multiple class names separated by white space. Here's a quick example:

 	.my-class{
		 color : red;
		 width:500px;
		 border: 1px solid black;
	}   
	
`[attr]` : This selector will select all elements with the attribute attr, whatever its value.
`[attr=val]` : This selector will select all elements with the attribute attr, but only if its value is val.
`[attr~=val]`: This selector will select all elements with the attribute attr, but only if  val is one of a space-separated list of words contained in attr's value. 



[attr^=val] : This selector will select all elements with the attribute attr for which the value starts with val.
[attr$=val] : This selector will select all elements with the attribute attr for which the value ends with val.
[attr*=val] : This selector will select all elements with the attribute attr for which the value contains the substring val. (A substring is simply part of a string, e.g. "cat" is a substring in the string "caterpillar".) 

	
##### Declaration
   	 
  choose what properties of the element you want to change `color:red`

#####  Propreties 

color is the property and `<p>` is the tag   

##### Property vaule

`red` and others


 each set must be wrappered in
 curly braces `({})`.
  
  with each declaration you must use a semicolon :
  
  with each rule set you must end ;

   
  
# JQuery 

### what is Jquery

free, open-source javascript library  
simplifies web development tasks
Ajax Content manipulation animations

smooth over cross-browser development issue
concise easy to read syntax


 
   include jquery
   
   	<script scr="../jquery-3.0.0.js"></script>
   	
	   	<script>
		   	$("docment").ready(function( ){
		   		$("#content").append("<p> the page just loaded
		   		</p>");
		   	})
	   	</script>
	  
	
		  

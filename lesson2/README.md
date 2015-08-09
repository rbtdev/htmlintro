# Lesson 2
## Bringing Javascript, CSS, and HTML together

This lesson will focus on tying together HTML document structure, CSS styling, and adding dynamic content using Javascript.  Building on the Lesson 1 HTML template, the student will extend the HTML document to add more structure, add additional styles using CSS, and introduce Javascript functions to add dynamic behavior to the web page.

## Intro to Javascript

Whereas HTML provides a static structure for a web page, Javascript provides the ability to dynamically interact with the user, modify the web page structure, and update CSS styles dynamically.  Unlike HTML, Javascript is a full featured programming language. Originally developed to provide very basic scripting capabilities for static web pages, Javascript has evolved to become a programing language capable of supporting the development of full featured web applications.  

### The Document Object Model
Understanding mechanics of how Javascript works requires some insight into how a web browser loads and renders a static HTML document.  When a browser loads a URL (either from a remote server, or from a local filesystem), it parses the HTML document and creates an internal structure for the web page called the Document Object Model or DOM.  The DOM exists in the browser's memory and is used by the browser to render the visual representation of the web page.  Each "tag" in an HTML document (`<div>`, `<p>`, `<ul>`, etc...) is converted into an internal represtnation called a DOM 'element'. Becuase the DOM is an in-memory representation of the original HTML document, it can be modified at any time, thus changing the rendered (visual) web page (even though the original HTML document is not changed). As will be explained late, Javascript provides specific functions to access and change the DOM for just this purpose.

### Adding Javasctipt to HTML
As the browser parses the HTML document, if it encounters a `<script>` tag it will interpret everything up until the `</script>` tag as Javascript.  For the purposes of this initial use of Javascript we will embedd our code directly in the HTML document. However for more advanced uses of Javascript we can put all of our code in separate files for better organization and structure of our Javascript code.  By adding the 'src' attribute to the `<script>` tag (`<script src = 'someurl'>`) the browser will load the references URL as Javascript and interpret it as if it were embedded directly int the HTML. The `<sript>` tag can appear anywhere in an HTML document, and can appear multiple times througout an HTML document.

### Javacript Language Basics

#### Variables or `var`
The fundamental entity in Javascript is a variable.  To declare a variable simply use the keyword `var` followed by an identifier for the variable. For example:

```javascript
var myName = "Robert Thuleen"
```
declares a variable (var) named 'myName' which contains the value "Robert Thuleen". This is an example of a "string" variable.  Variables can contain numeric, string, array, or more complex "objects" which can be defined by the programmer to represent complex data.  More on this in later lessons. Once a variable has been declared and contains a value, it can be used in javacript code either by accessing that value, or changing it.

#### Functions
The easiest way to understand functions is to consider them as blocks of re-useable Javascript. Once a function is defined, it can be called upon to perform the same steps any number of times without having to type the same code in many different places.  For example:

```javascript
var add = function (a, b) {
	var c = a + b;
	return c;
}
```


### The 'document' Object
As mentioned above, once the browser has loaded the HTML file it converts the HTML into an internal representation called the DOM.  The DOM is available to Javascript functions by referencing the 'document' object. 

#### Example
Drawing from the HTML document from lesson 1: 

```html
<html>
	<head>
	<style>
		.title {
			color: red;
		}
	</style>
	</head>
	<body>
		<div class = 'title'>
			Hello World!!
		</div>
	</body>
</html>
```
The goal of this example is to update the lesson 1 html to add a simple javascript function which will take the place of the string "Hello World!!".  
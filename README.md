# Lesson 2
## Bringing Javascript, CSS, and HTML together

This lesson will focus on tying together HTML document structure, CSS styling, and adding dynamic content using Javascript.  Building on the Lesson 1 HTML template, the student will exhance the HTML document to add more structure, add additional styles using CSS, and introduce Javascript functions to add dynamic behavior to the web page.

## Intro to Javascript

Whereas HTML provides a static structure for a web page, Javascript provides the ability to dynamically interact with the user, modify the web page structure, and update CSS styles dynamically.  Unlike HTML, Javascript is a full featured programming language. Originally developed to provide very basic scripting capabilities for static web pages, Javascript has evolved to become a programing language capable of supporting the development of full featured web applications.  

### The Document Object Model
To understand the mechanics of how Javascript works requires some insight into how a web browser loads and renders a static HTML document.  When a browser loads a URL (either from a remote server, or from a local filesystem), it parses the HTML document and creates an internal structure for the web page called the Document Object Model or DOM.  The DOM exists in the browsers memory and is used by the browser to render the visual representation of the web page.  Each "tag" in an HTML document ('div', 'p', 'ul', etc...) is converted into an internal represtnation called a DOM 'element'.

### Adding Javasctipt to HTML
As the browser parses the HTML document, if it encounters a `<script>` tag it will interpret everything up until the `</script>` tag as Javascript.  For the purposes of this initial use of Javascript we will embedd our code directlu in the HTML document. However for more advances uses of Javascript we can put all of our code in separate files for better organization and structure of our Javascript code.  By adding the 'src' attribute to the `<script>` tag (`<script src = 'someurl'>`) the browser will load the references URL as Javascript and interpret it as if it were embedded directly int the HTML.

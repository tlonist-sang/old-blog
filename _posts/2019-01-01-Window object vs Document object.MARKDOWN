---
layout: post
title:  "Window? Document? stop confusing me"
date:   2018-12-30 12:00:00 +0900
comments: true
categories: Javascript
---

This posting will answer the following questions.

0. Broad Definition
1. What does it do?
2. What do I want to know?
3. Some facts

[Window]

0. What is a window object?

: is an object that contains browser components, javascript engine, and 'all' variables.
: is responsible for the whole of what is going on in the browser.
: is a global object and an ancestor of all the objects. 
: is an object that is supported by all browsers (one of Browser Object Models)

1. What does the window object do?

	Typing window + . in chrome debugger pops up many itmes, each of which is related to what window object can do. Here are some common examples. 

	- Opening, closing, and adjusting the window : 
			window.open(), window.close(), window.innerHeight .. etc
	
	- Setting time for execution: 
			window.setTimeout(), window.setInterval()
	
	- Url related functions: 
			window.location.href, window.encodeURI()

	- Navigator:
			browser information (language, browser type, GPS, batter check .. etc)

	- Document:
			Document object is actually a sub-item of the window object! This will be dealt below.

2. What do I want to know more? 

	I've often encoutered this object with onload() method. 
	window.onload is fired when the entire page loads, including its content(images, css, scripts, etc)
	https://stackoverflow.com/questions/588040/window-onload-vs-document-onload

3. Some facts
	
	- Since it is a global variable, writing window is typically omitted.

[Document]

0. What is a document object?

: controls HTML.
: is the root node of the HTML document.

1. What does the document object do?

	As was written above, most of its functions deal with HTML manipulation.

	- Finding DOM element with specific ID:
		document.getElementById(), document.querySelector() .. etc

	- Accessing different parts of HTML:
		document.head, document.body, document.title

	- User actions:
		document.onmouseup, document.onkeyup .. etc

2. What do I want to know more?
	
	$(document).ready(function(){}) http://learn.jquery.com/using-jquery-core/document-ready/
	document.onload is called when the DOM is ready, which can be prior to images and other external sources that should be loaded. Code included inside will only run once the page Document Object Model is ready for javascript code to execute; hence it is different from $(window).on("load", function()) in terms of the execution timing.  

	<html>
	<head>
	    <script src="https://code.jquery.com/jquery-1.9.1.min.js"></script>
	    <script>
	    $( document ).ready(function() {
	        console.log( "document loaded" );
	    });
	 
	    $( window ).on( "load", function() {
	        console.log( "window loaded" );
	    });
	    </script>
	</head>
	<body>
	    <iframe src="http://techcrunch.com"></iframe>
	</body>
	</html>


	



[jekyll-docs]: https://jekyllrb.com/docs/home
[jekyll-gh]:   https://github.com/jekyll/jekyll
[jekyll-talk]: https://talk.jekyllrb.com/

---
layout: post
title:  "Window? Document? stop confusing me"
date:   2018-12-30 12:00:00 +0900
comments: true
categories: JavaScript
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


<div class="colorscripter-code" style="color:#010101; font-family:Consolas, 'Liberation Mono', Menlo, Courier, monospace !important; position:relative !important; overflow:auto"><table class="colorscripter-code-table" style="margin:0; padding:0; border:none; background-color:#fafafa; border-radius:4px;" cellspacing="0" cellpadding="0"><tr><td style="padding:6px; border-right:2px solid #e5e5e5"><div style="margin:0; padding:0; word-break:normal; text-align:right; color:#666; font-family:Consolas, 'Liberation Mono', Menlo, Courier, monospace !important; line-height:130%"><div style="line-height:130%">1</div><div style="line-height:130%">2</div><div style="line-height:130%">3</div><div style="line-height:130%">4</div><div style="line-height:130%">5</div><div style="line-height:130%">6</div><div style="line-height:130%">7</div><div style="line-height:130%">8</div><div style="line-height:130%">9</div><div style="line-height:130%">10</div><div style="line-height:130%">11</div><div style="line-height:130%">12</div><div style="line-height:130%">13</div><div style="line-height:130%">14</div><div style="line-height:130%">15</div><div style="line-height:130%">16</div><div style="line-height:130%">17</div></div></td><td style="padding:6px 0"><div style="margin:0; padding:0; color:#010101; font-family:Consolas, 'Liberation Mono', Menlo, Courier, monospace !important; line-height:130%"><div style="padding:0 6px; white-space:pre; line-height:130%">&lt;html&gt;</div><div style="padding:0 6px; white-space:pre; line-height:130%">&lt;head&gt;</div><div style="padding:0 6px; white-space:pre; line-height:130%">&nbsp;&nbsp;&nbsp;&nbsp;&lt;script&nbsp;src="https://code.jquery.com/jquery-1.9.1.min.js"&gt;&lt;/script&gt;</div><div style="padding:0 6px; white-space:pre; line-height:130%">&nbsp;&nbsp;&nbsp;&nbsp;&lt;script&gt;</div><div style="padding:0 6px; white-space:pre; line-height:130%">&nbsp;&nbsp;&nbsp;&nbsp;$(&nbsp;document&nbsp;).ready(function()&nbsp;{</div><div style="padding:0 6px; white-space:pre; line-height:130%">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;console.log(&nbsp;"document&nbsp;loaded"&nbsp;);</div><div style="padding:0 6px; white-space:pre; line-height:130%">&nbsp;&nbsp;&nbsp;&nbsp;});</div><div style="padding:0 6px; white-space:pre; line-height:130%">&nbsp;</div><div style="padding:0 6px; white-space:pre; line-height:130%">&nbsp;&nbsp;&nbsp;&nbsp;$(&nbsp;window&nbsp;).on(&nbsp;"load",&nbsp;function()&nbsp;{</div><div style="padding:0 6px; white-space:pre; line-height:130%">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;console.log(&nbsp;"window&nbsp;loaded"&nbsp;);</div><div style="padding:0 6px; white-space:pre; line-height:130%">&nbsp;&nbsp;&nbsp;&nbsp;});</div><div style="padding:0 6px; white-space:pre; line-height:130%">&nbsp;&nbsp;&nbsp;&nbsp;&lt;/script&gt;</div><div style="padding:0 6px; white-space:pre; line-height:130%">&lt;/head&gt;</div><div style="padding:0 6px; white-space:pre; line-height:130%">&lt;body&gt;</div><div style="padding:0 6px; white-space:pre; line-height:130%">&nbsp;&nbsp;&nbsp;&nbsp;&lt;iframe&nbsp;src="http://techcrunch.com"&gt;&lt;/iframe&gt;</div><div style="padding:0 6px; white-space:pre; line-height:130%">&lt;/body&gt;</div><div style="padding:0 6px; white-space:pre; line-height:130%">&lt;/html&gt;</div></div><div style="text-align:right; margin-top:-13px; margin-right:5px; font-size:9px; font-style:italic"><a href="http://colorscripter.com/info#e" target="_blank" style="color:#e5e5e5; text-decoration:none">Colored by Color Scripter</a></div></td><td style="vertical-align:bottom; padding:0 2px 4px 0"><a href="http://colorscripter.com/info#e" target="_blank" style="text-decoration:none; color:white"><span style="font-size:9px; word-break:normal; background-color:#e5e5e5; color:white; border-radius:10px; padding:1px">cs</span></a></td></tr></table></div>
	



[jekyll-docs]: https://jekyllrb.com/docs/home
[jekyll-gh]:   https://github.com/jekyll/jekyll
[jekyll-talk]: https://talk.jekyllrb.com/

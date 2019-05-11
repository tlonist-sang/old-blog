---
layout: post
title:  "What is NodeJS"
date:   2019-04-16 12:00:00 +0900
comments: true
categories: JavaScript
---

#What is NodeJS?

In this posting, I will write about what NodeJS is.
It will be sort of like a summary of the posting below.
(https://medium.freecodecamp.org/what-exactly-is-node-js-ae36e97449f5)

###Table of contents
- Gibberish
- Before Node.js 
- Now with Node.js
- Why use Node.js

There seem to be so many technologies that have something to do with Javascript. NodeJS was just one of them for me, until I was forced to explain what it really was to a close friend of mine.

That time, I somehow likened it to Tomcat, because I remember to have used it 'sort of' like a servlet container that enables codes with JavaScript act like backend logic. The questions followed, however, and hence was drying the shallowness of my erroneous understanding. So here I am writing a post about it.

>>"What JRE is to Java is what Node.js is to JavaScript".
This pretty much sums it up. Here is a good diagram that help understand this already pretty obvious explanation.

![img]({{ "/assets/img/nodejs diagram.png" | absolute_url }})


**Before Node.js...**
- JavaScript was a script lanaguage interpreted by Browsers
- JavaScript's main function was to enable dynamic communication between client and the browser.

**Now with Node.js...**
- JavaScript is no more a mere script language, but a stand-alone runtime environment
- It means that JavaScript can take over what used to be exclusively done by the server-side languages like Java or PHP.

**Why use Node.js?**

1. It is used by V8 Engine.
- V8 engine takes JavaScript code and converts it into a faster machine code that can be run without interpretation. (very fast!)
- V8 engine will be continuously upgraded as long as Google persists. 

2. It is event-driven.
- It minimizes the resources needed to listen to a user's event request by connecting and triggering the event only when the user makes the call. 

3. non-blocking I/O
![img]({{ "/assets/img/io nio.png" | absolute_url }})

- Unlike blocking I/O, which occupies all modules while read/write events are taking place (in other words, you can't do anything in between), non-blocking I/O is set to 'ready' mode as soon as Read/Write event start. Hence it is faster and uses less memory

4. Single Thread (just look it up)

√√√
Hello NodeJS! (formatting syntax test)
√√√


[jekyll-docs]: https://jekyllrb.com/docs/home
[jekyll-gh]:   https://github.com/jekyll/jekyll
[jekyll-talk]: https://talk.jekyllrb.com/

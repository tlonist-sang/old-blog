---
layout: post
title:  "Java Web Module Structure"
date:   2019-01-08 12:00:00 +0900
comments: true
categories: Java
---

Searching through already-made web projects in the workplace, I have always wondered the functions of each directories that were composing the project. I heard only briefly that there is a specification document which defines the usages of things like those. There indeed was one (https://download.oracle.com/otn-pub/jcp/servlet-2.4-fr-spec-oth-JSpec/servlet-2_4-fr-spec.pdf?AuthParam=1546950640_7caec6a7bcffd7161ee994e7d7751fc5); and before delving into it (I will actually peruse it), I found a rather shorthand explanation of my curiosity from a document from Oracle. (https://docs.oracle.com/cd/E19226-01/820-7627/bnadx/index.html). 

In this posting I will provide
1. Brief recap of the aforementioned shorthand explanation of my curiosity
2. 1 is just about it :P


1. Recap of [Web Module Structure]

- Web module has a specific structure. Top level directory of the structure is called document root. 
- The document root contains a subdirectory named 'WEB-INF', which contains the following files and directories. 
	- web.xml : web application deployment descriptor
	- classes : directory that contains server-side classes
	- tags : directory that contains tag files
	- lib : directory that contains JAR archives of libraries called by server-side classes.

![img]({{ "/assets/img/web-module.gif" | absolute_url }})


- If a web module contains only XHTML pages and static files, web.xml is not needed.
- a web module can be packaged in a JAR file known as a web archive (WAR) file. The contents and user of WAR files differ from those of JAR files, WAR file names use a .war extension. The web module just described in portable; and one can deploy it into any web container that conforms to the 'Java Servlet Specification'!.

[Making it solid : Difference between WAR and JAR] (https://stackoverflow.com/questions/5871053/difference-between-jar-and-war-in-java)

- JAR: It contains "libraries, resources and accessories files".
- WAR: It contains a "web application" that can be deployed to any servlet/jsp container (it comprises of jsp, html, javascript.. etc).

- Setting the Context Root
	- A context root identifies a web application in a Java EE server. It must start with a forward slash and end with a string. 


This was a rather-too-brief summary of what I read. Being a web engineer (or to be entitled to say so), I think it is also necessary to review how the Tomcat, the most well-known servlet container, works by investigating some of its codes. I hope I could write several posts regarding that topic before summer arrives.

[jekyll-docs]: https://jekyllrb.com/docs/home
[jekyll-gh]:   https://github.com/jekyll/jekyll
[jekyll-talk]: https://talk.jekyllrb.com/

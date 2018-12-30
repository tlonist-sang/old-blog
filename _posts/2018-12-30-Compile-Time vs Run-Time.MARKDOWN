---
layout: post
title:  "Compile time and Run time"
date:   2018-12-30 12:00:00 +0900
comments: true
categories: Java
---

Having a firm understanding about what is runtime/compile time is very important in developing. I'd like to clear up the distinction between these two. This is pretty much my regurgitation of a good source (https://stackoverflow.com/questions/846103/runtime-vs-compile-time). Two concepts could be analyzed by four questions as below:

1. What are the inputs and outputs of this phase?
2. What factors can cause problems in this phase?
3. If this succeeds, what do we know?

[Compile Time]

1. Input and Output: 
	Input is whatever is needed for the program to be compiled; such as codes, interfaces, libraries. Output is the result of the compiling; that is assembly code or relocatable object code, etc. If compiling fails, output creates error messages and the program is certainly not executable. 

2. Possible problems:
	Syntax erros, Typechecking erros, Compiler crashes.

3. If compiler succeeds, what do we know?
	Program has no erros mentioned in 2 above - that the program is well formed.
	It is possible to run the program without issues in compiling.


[Run Time]

1. Input and Output:
	Input: All kinds of user input (filling up a registration form, network packets, jobs sent to printer)
	Output: All kinds of output that the program is designed to fulfill 

2. Possible problems:
	Division by zero, Running out of memory, Dereferencing a null pointer(trying to access a null pointer address)
	Trying to open a file that doesn't exist, Trying to find a web page that is malfunctioning.

3. If run-time succeeds, what do we know?
	We know that the program is functioning without under given input; but whether we have the desired output is upto the codes. 




[jekyll-docs]: https://jekyllrb.com/docs/home
[jekyll-gh]:   https://github.com/jekyll/jekyll
[jekyll-talk]: https://talk.jekyllrb.com/

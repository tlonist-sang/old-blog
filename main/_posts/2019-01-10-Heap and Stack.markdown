---
layout: post
title:  "Heap and Stack"
date:   2019-01-10 12:00:00 +0900
comments: true
categories: Java
---

I will review the concepts of heap and stack here. Through this posting I will clarify
1. Definition of heap and stack
2. Major differences (+ stuffs worth knowing)
(https://stackoverflow.com/questions/79923/what-and-where-are-the-stack-and-heap)
(https://www.programmerinterview.com/index.php/data-structures/difference-between-stack-and-heap/)



1. Definitions
	
	1-0. What's common?
	- They are both stored in computer's RAM(Random Access Memory)

	1-1. Heap
	- Memory set aside for dynamic allocation. There is no pre-figured pattern for allocation or de-allocation of blocks from heap. One ca n allocate and free  block at any time. This makes it a rather complex task to keep track of which parts of the heap are allocated or freed at any given point in time; there are many custom heap allocators available to tune heap performance for different usages.


	1-2. Stack
	- Memory set aside as a scratch space for a thread of execution. When a function is called, a block of memory is reserved on the top of stack for local variables and some book-keeping data. When the function returns, the block is made unused and can be used when a function(not necessarily the same one) is called next time. Stack works in a Last In First Out order, meaning the most recently used one is always the one that is freed first. Freeing a block from the stack is like adjusting one pointer.

2. Major differences and stuffs worth knowing

	[Where are they typically attached to?]
	- Each thread gets a stack, while there's typically one heap for an application (It is not uncommon to have multiple heaps for different types of allocation)

	[What are their scopes?]
	- Stack is attached to a thread; so when the thread terminates it is reclaimed. The heap is typically allocated at the start of an application by the runtime, and is reclaimed when the application exits. While the program is being executed, however, unless it is freed manually, the allocated heap memory persists. 

	[What determines the size of each of them?]
	- The size of stack is set when a thread is created. Typically it is set fixed, hence if there is not enough space, a stack overflow occurs. (typically seen when there is infinite or too many recursive calls) The size of heap is set on application startup, but can expand as more space is needed.

	[Which is faster?]
	- The stack is faster because the pattern of its allocating and freeing memory, which is just a pointer increment or decrement, is much simpler than that of heap, which has to do with whole of complex book-keeping process of allocation and freeing. Moreover, each byte in stack tends to be mapped to processor's cache, making it faster. 
	- Because data in heap is mostly a global resource, it has to be multithread safe, meaning each allocation and freeing has to be synchronized with all other heap accesses in the program, making it much slower that stack.




[jekyll-docs]: https://jekyllrb.com/docs/home
[jekyll-gh]:   https://github.com/jekyll/jekyll
[jekyll-talk]: https://talk.jekyllrb.com/

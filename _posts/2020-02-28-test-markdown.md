---
layout: post
title: Effective Coding - Part 1
subtitle: Being a more effective programmer
gh-repo: daattali/beautiful-jekyll
gh-badge: [star, fork, follow]
tags: [coding, blod]
comments: true
---

Throughout my academic and professional career, I've made many missteps during the software development process. Some of these
missteps lead to hours of debugging, or throwing away hundreds of lines of code. While these situations can be frustrating, they are
also learning opportunities. So I would like to share some of the lessons I've learned on how to be a more effective programmer
	
In this post, I will focus on how an individual can be more effective when writing code, regardless of the application. Whether you are
focused on network automation (as I am), or building a web application, these principles will broadly apply to most programming paradigms.
I will not focus on the dynamics of working on a shared codebase with a team, but I do plan to cover that topic in a future post. I

**Pick the right tools for the job**

	Its a cliche for a reason. Before starting on a new project, you should always take some time to consider what is the most
appropriate toolset for your use. This starts with choosing a programming language. You might choose Python if you're doing network
automation, or AI/ML. Javascript is a common choice for building a front-end for an application. Or if you're doing data analysis, you
might use something like R. Many modern programming languages are general purpose and can meet a wide variety of use cases, but its
worth your time to do a bit of research to see what language best aligns with you're requirements. Think about the type of application,
how complex it needs to be, who will be using it, performance and security requirements, etc.
	
	Also, take some time to look into existing libraries for chosen language that can help to meet your use case.
DON'T REINVENT THE WHEEL. For example, if you need to retrieve data from a system using an HTTP API, see if there is 
an API client library for that system. A well-written API client library will provide useful abstrations that can significantly reduce
the amount of code that you will need to write.

**Plan your sessions**

## "Weeks of coding can save hours of planning." -Unknown

	When working on a new body of code, or refactoring an existing one,  a little bit of planning can go a long way. Of course for a large project, 
you need to think about use cases, architecture, schedule, etc. But what I'm talking about here is at more of a micro level: how can you plan for an 
individual coding session to be effective and efficient. For example, if I want to automate some task, I might start with a brainstorming session.
I'll thinking about what the inputs and outputs are. This helps to frame the problem and I can begin getting a general idea
of how the program might flow. I find it helpful at this step to write some pseudo-code, or sketch something down on a notepad.
Once I have a general idea of how the program might flow, I like to break things down into sub-processes. For example, I need to retrieve data
from System 1, perform transformations x,y, and z, then write the newly transformed data to System 2. I can then write function stubs for each
of these to fill out later. This provides a nice skeleton, and I can then start implementing the business logic. 

	The way I think about this process is that you start with a high level, somewhat abstract idea of what your code needs to do, and then slowly work towards a 
concrete implementation. I've noticed that as I've practiced and improved at this process, my brain will start to automatically layout and organize a program before 
I've even began the implementation process.


**Read documentation**

	I had a college professor who said that the difference between a good programmer and a great one is that a great programmer reads
documentation. It's easy to turn to documentation when you're looking for a very speficic thing, and you can just ctrl-f search a function name 
to find the correct data type for an input. But I would recommend taking some time to sit and get familiar with the documentation of any
tool that you are going to be using frequently. For me it was the Python Standard Library docs. Reading that documentation has made me a much
more effective Python programmer. Technical documentation can be quite dull to read, so I would generally do it in small chunks. Also, I would keep my
IDE open alongside the documentation, so that I could experiment with some of the structures, and put what I'm reading directly into practice.


**Strive for readability**
	Readability is critical to writing good, clean code. When your code is readable, its easy to understand. This means its also easy to extend or modify. I've had
the experience of looking back at code I had written just a few years prior and being unable to make much sense of it. Functions were poorly organized, comments were lacking,
variable names were non-descript, etc. If I can't understand my own code, I definitely can't expect another developer to understand it. Even when working on a solo project, if you write
readable code, your future self will thank you. If you're working on a shared codebase with a team, readability is even more important. 

	Aim to write code that is so clean that it serves as its own documentation. Here's an example from a stackoverflow post (linked below).
	
	`float a, b, c; a=9.81; b=5; c= .5*a*(b^2);`
	
	vs
	
	`float computeDisplacement(float timeInSeconds) {
		const float gravitationalForce = 9.81;
		float displacement = (1 / 2) * gravitationalForce * (timeInSeconds ^ 2);
		return displacement;
	}`
	
	These two code snippets are doing the same calculation, but the latter is much clearer with descriptive variable names and a descriptive name for the function. The code itself tells
you what its doing. Now that doesn't mean we throw out comments entirely. Its generally a good idea to write docstring comments for all your classes, methods, etc. But favor code that is clear
and understandable. A readable solution that's 5 lines of code is generally preferred to a hacky 1 line solution. 

	
I hope you enjoyed this post and found it useful. Feel free to reach out to me via email if you have questions, comments, or suggestions for future posts.
	
	

	Links:
	https://stackoverflow.com/questions/209015/what-is-self-documenting-code-and-can-it-replace-well-documented-code
	https://programmerhumor.io/programming-memes/when-reading-docs-and-closing-the-tab-immediately-2/

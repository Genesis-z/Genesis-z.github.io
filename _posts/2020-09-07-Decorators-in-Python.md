---
layout: post
title:  "Decorators in Python"
author: john
categories: [ Python ]
comments: True
image: assets/images/decs2.jpeg
beforetoc: "Decorators in Python"
toc: false
featured: true
---

Recently we came across this catchy concept in python and we thought it would be helpful on writing some basic stuffs about this. So lets dive in!!!

In simple fancy terms, decorators in python would decorate the function to which is it destined in the code. Often referred as `syntactical sugar`, this does modifies a function or a class without changing any of its code. At first it might be hard to get this, but once you've figured its purpose it will be a much easier while exploring its complexity.

**Quick Note**: In python, functions are handled similarly like objects. Means...you can assign a function to variable and execute the function by calling that variable.

Consider `function1()`. This can be assigned to a variable 
```shell
var = function1 #stores address of function1 in var
var()
```
Or if you just want the value of `function1` to be stored in the variable, then 
```shell
var = function1()
```


We've briefed what decorators could do, with a code snippet below

```shell
#This is our decorator
def decorator(func)
	def wrapper()
		print("Before Execution of func")
		func()
		print("After Execution of func...Bye")
	return wrapper

@decorator
def func()
	print("hey there")

#execution	
func()
```
On execution this outputs,

```shell
Before Execution of func
hey there
After Execution of func...Bye
```

From this we could get some basic understanding on decorators. We have a funcion func(). Without explicitly calling decorator in execution, we extended func() to have(here 'print') something more.

Before getting to a deeper understanding into this, let see how we could have done this in python without decorator,

```shell
#This is our decorator
def decorator(func)
	def wrapper()
		print("Before Execution of func")
		func()
		print("After Execution of func...Bye")
	return wrapper

def func()
	print("hey there")
#execution
func()

doing_decoration = decorator(func)
doing_decoration()
```
While calling `decorator(func)`, inline function will also gets called and from code it is evident that we are returing `wrapper`(address of wrapper). Hence execution of `doing decoration()` technically does calls `wrapper` function. Just have this in mind. This will be helpful while we see about 'passing arguments' to decorator function.

Both of the above code snippets does the same. With decorator syntax we just replaced 
```shell
doing_decoration = decorator(func)
doing_decoration()
```
This might seem to be couple of lines. But if your code has bunch of functions and needs some actions repeatedly done on all functions, then decorators comes in hand.

Now lets talk about passing arguments. Consider our `func1` has some arguments to pass,
```shell
@decorator
def func(name)
	print("hey there {}".format(name))
```
If you run this, this would throw an error. Because, `decorator` takes a function as argument and `wrapper` does not takes any arguments. Remember we said, on calling `decorator()` it calls wrapper function. We can resolve this with help of `*args` and `**kwargs` included in wrapper function. 

Modify your wrapper function as 
```shell
def wrapper(*args, **kwargs)
```
This should do the purpose. With this the wrapper function can handle any number of parameters passed.

We have covered the necessary basics of decorators here. There are lot of use cases like debugging, multiple(repeated) print statements etc for decorators and some cases could be done without decorators too. It all depends on your code. 

One of my favorite decorator would be the timer decorator. This returns the time taken for execution. I have included multiple decorators for fun. You'll understand this easily by going through the below code.

<p><script src="https://gist.github.com/Grim97/c1c218c4933be7076321fba2ba72ad2d.js"></script></p>

So, that's all for this post. Hope you guys liked it. Do share and support!!!




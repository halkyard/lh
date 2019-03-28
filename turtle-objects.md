---
title: Turtle
description: Everything in Python is an object
---
# Introduction to python objects through Turtle graphics
Everything in Python is an object.  We'll use the turtle demo to explore basic data types because:
*   it can be boring to learn building blocks without making anything
*   it helps to visualize abstract concepts with concrete examples

It is also good to reinforce the principle that it is possible to learn topics of interest through python packages.  Again, we'll use IDLE, not because it is the best development environment in the world, but because it's written in python and cross platform.  

## Resources

*    [Turtle Geometry: The Computer as a Medium for Exploring Mathematics - Artificial Intelligence](https://www.amazon.com/gp/product/0262510375)
*    [Turtle docs](https://docs.python.org/3.3/library/turtle.html?highlight=turtle)
*    [Al's turtle stuff](https://github.com/asweigart/art-of-turtle-programming)

## Importing the Zen of python

Python modules or programs are also objects and can imported.  Try:

```
import this
The Zen of Python, by Tim Peters

Beautiful is better than ugly.
Explicit is better than implicit.
Simple is better than complex.
Complex is better than complicated.
Flat is better than nested.
Sparse is better than dense.
Readability counts.
Special cases aren't special enough to break the rules.
Although practicality beats purity.
Errors should never pass silently.
Unless explicitly silenced.
In the face of ambiguity, refuse the temptation to guess.
There should be one-- and preferably only one --obvious way to do it.
Although that way may not be obvious at first unless you're Dutch.
Now is better than never.
Although never is often better than *right* now.
If the implementation is hard to explain, it's a bad idea.
If the implementation is easy to explain, it may be a good idea.
Namespaces are one honking great idea -- let's do more of those!
```

## Import turtle

Importing turtle can be done in the same way.  The module is written using the gui package tkinter.  Let's view and interact with a turtle object through IDLE.

```py
from turtle import *
mode('logo')
showturtle()
```

This opens a window and shows the turtle in logo mode.  The motion and drawing commands are:

| command | alias |
| :--- | :--- |
|showturtle()| st() |
|hideturtle()| ht() |
| forward()  | fd() |
| backward() | bk() |
|rightturn() | rt() |
|leftturn()  | lt() |
|penup()  | pu() |
|pendown()  | pd() |

![0](/sh/assets/images/turtle0.png?raw=true)

*    credit to Allen Downey http://www.allendowney.com/wp/ for shapes.py below, any mistakes are mine

```py
# shapes.py
from turtle import *
mode('logo')
reset()

# This is a comment
""" This is
a multi line
comment
"""
## see Format for comment toggling options

# Make a square

##fd(100)
##rt(90)
##fd(100)
##rt(90)
##fd(100)
##rt(90)
##fd(100)
##rt(90)

# range

## help(range)
## range(4)
## for i in range(4): print("Hi!")
## for spam in range(4): print("eggs!")
## for spam in range(4): print(spam)
## for spam in "eggs": print(spam)

# Defining a Function

def square():           # indentation matters in python
    fd(100)
    rt(90)
    fd(100)
    rt(90)
    fd(100)
    rt(90)
    fd(100)
    rt(90)

# square()

# Using a loop

def square():
    for i in range(4):  
        fd(100)         # nested indentation
        rt(90)

# square()

# Pass in an argument

def square(size):
    for i in range(4):  
        fd(size)         
        rt(90)

# square(200)

def triangle(size):
    for i in range(3):
        fd(size)
        rt(120)

def polygon(size, sides):
    for i in range(sides):
        fd(size)
        rt(360 / sides)

def house(size):
    square(size)
    fd(size)
    rt(30)
    triangle(size)

def boxes(size):
    for i in range(6):
        for j in range(6):
            fd(size)
            rt(60)
        rt(60)

def star(size):
    for i in range(5):
        fd(size)
        rt(144)
        fd(size)
        lt(72)

def star_group(size):
    for i in range(6):
        star(size / 4.0)
        pu()
        fd(size)
        pd()
        rt(60)

def super_star_group(size):
    for i in range(4):
        star_group(size)
        pu()
        fd(size / 2.0)
        pd()
        rt(90)

##speed(0)  # 1 = slow, 10 = fast, 0 = fastest
##super_star_group(100)
```
## Turtle demo

In the IDLE shell go to: `Help > Turtle Demo` and run through the examples.

![1](/sh/assets/images/turtle1.png?raw=true)

## Debug final example yinyang

*    copy the script from the final example to the clipboard
*    paste into a `File > New File`
*    save in the code directory
*    turn on `Debug > Debugger`
*    check the Source and Globals boxes

## Step through peace.py
## Step through yinyang.py
## Step through paint.py
## Create some shapes
### Make a square
### Power of looping
#### While
#### For
## Dictionaries and Classes
## Step through lindenmeyer anklets of krishna 

[]    indenting
[]    comments
Reading well written code will help us to think in a more 'pythonic' way.

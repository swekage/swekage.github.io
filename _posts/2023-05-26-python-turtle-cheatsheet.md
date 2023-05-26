---
published: true
---
---
layout: post
categories: [Technical]
---

![python turtle cheatsheet.png]({{site.baseurl}}/_posts/python turtle cheatsheet.png)

`turtle` is a preinstalled library in python that allows you to draw graphics. Many beginner computer science courses use it to teach students because it is easy to set up and use. 

I made this cheatsheet because one day, I was tutoring a student who needed to use python turtle to draw the US Flag. They were getting stuck on how to add color, and I asked them if they were provided any references to use when they got stuck. They said yes and showed me a link that their teacher gave them to the official python turtle documentation. I told him to click the link. What I saw was god awful. If you don't believe me, take a look for [yourself](https://docs.python.org/3/library/turtle.html) 😤😤

Hopefully this cheatsheet is more clear and will help you understand how to use turtle faster!

#### Table of Contents

Basics

- [Import turtle and set up turtle object](#import-turtle-and-set-up-turtle-object)
- [Move turtle](#move-turtle)
- [Turn turtle](#turn-turtle)
- [goto and home](#goto-and-home)
- [Pen up and down](#pen-up-and-down)

Drawing Shapes

- [Draw a Square](#draw-a-square)
- [Draw a Rectangle](#draw-a-rectangle)
- [Draw a Circle](#draw-a-circle)
- [Draw a Dot](#draw-a-dot)
- [Draw a Star](#draw-a-star)

Color

- [Changing the Screen Color](#changing-the-screen-color)
- [Changing the Pen Color](#changing-the-pen-color)
- [Filling in a Shape With Color](#filling-in-a-shape-with-color)

Pen Properties

- [Changing the Pen Speed](#changing-the-pen-speed)
- [Changing the Pen Size](#changing-the-pen-size)
- [Shorthand for Changing Pen Properties](#shorthand-for-changing-pen-properties)

Clear and Reset

- [Clear the Screen](#clear-the-screen)
- [Reset](#reset)


## Import turtle and set up turtle object

```python
import turtle

turtle.title('My Turtle Program')

t = turtle.Turtle()

t.forward(100)
```


## Move turtle

You can move the turtle forward or backwards a particular distance

```python
t.forward(100)

t.backward(100)
```

Use the shorthand versions if you get tired of writing out **forward** and **backward**

```python
t.fd(100)

t.bk(100)
```

See **goto and home** for how to move the turtle with x and y coordinates


## Turn turtle

You can turn the turtle either right or left at a particular angle

```python
t.right(90)

t.left(90)
```

Shorthand versions

```python
t.rt(90)

t.lt(90)
```


## goto and home

You can also move the turtle by giving it x and y coordinates. The turtle always starts at (0,0) when you first start the program.

```python
t.goto(100,100)
```

You can always bring the turtle back to (0,0) using `t.home()`

```python
t.forward(100)
t.right(90)
t.forward(90)
t.home()
```

## Pen up and down

Sometimes you want to move the pen without drawing. Here's how you draw 2 parallel lines.

```python
t.forward(100)
t.right(90)
t.penup()

t.forward(100)
t.right(90)

t.pendown()
t.forward(100)
```

## Draw a Square

This is how you draw a square.

```python
t.forward(100)
t.right(90)
t.forward(100)
t.right(90)
t.forward(100)
t.right(90)
t.forward(100)
t.right(90)
```

or if you want to use a for-loop

```python
for i in range(4):
    t.forward(100)
    t.right(90)
```

## Draw a Rectangle

Similar to drawing a square

```python
t.forward(100)
t.right(90)
t.forward(30)
t.right(90)
t.forward(100)
t.right(90)
t.forward(30)
t.right(90)
```

## Draw a Circle

You can provide a radius to **t.circle()** to create a circle.

```python
t.circle(100)
```

## Draw a Dot

You can provide a diameter to the **t.dot()** to create a dot.

```python
t.dot(50)
```

## Draw a Star

```python
for i in range(5):
    t.forward(100)
    t.right(144)
```


## Changing the Screen Color

We can change the screen color on the imported turtle library

```python
import turtle

turtle.bgcolor('blue')
```

## Changing the Pen Color

```python
t.pencolor('red')
t.forward(100)
```

You can also use Hexcode

```python
# change pen color to green
t.pencolor('#008000')
t.forward(100)
```

or RGB

```python
# by default the colormode is 1. we need to change it to 255 to use typical rgb values.
# if we want to stay on 1, then we just need to divide each of the rgb values by 255.
turtle.colormode(255)

red = (255, 0, 0)
t.pencolor(red)
t.forward(100)
```

## Filling in a Shape With Color

```python
t.fillcolor('red')

t.begin_fill()
t.forward(100)
t.left(120)
t.forward(100)
t.left(120)
t.forward(100)
t.end_fill()
```

You can also use Hexcode

```python
# change pen color to green
t.fillcolor('#008000')
```

or RGB

```python
# by default the colormode is 1. we need to change it to 255 to use typical rgb values.
# if we want to stay on 1, then we just need to divide each of the rgb values by 255.
turtle.colormode(255)

red = (255, 0, 0)
t.fillcolor(red)
```

## Changing the Pen Speed

Sometimes you want the pen to move faster. 0 is the slowest. 10 is the highest.

```python
t.speed(10)
```

## Changing the Pen Size

Sometimes you want to have larger brush strokes

```python
t.pensize(10)
```

## Shorthand for Changing Pen Properties

It can be tedious to write everything out. Here's how you can do it with `t.pen()`

```python
t.pen(pencolor='red', fillcolor='green', pensize=5, speed=10)
```


## Clear the Screen

This clears the screen but leaves your turtle properties the same

```python
t.clear()
```

## Reset

This resets everything including the turtle properties

```python
t.reset()
```

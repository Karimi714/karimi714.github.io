---
layout: posts
title: See MY Project

## This is my painting with python
the picture is:
- my painting with the turtle library of python





![my painting](../assets/images/my_painting.jpg "painting")

---
**The Code of my painting**:
import turtle
import random

turtle.tracer(0)

def make_frame():
    turtle.pensize(17)
    turtle.pencolor("#301105")
    turtle.penup()
    turtle.setpos(-500,-300)
    turtle.pendown()
    for i in range(2):
        turtle.fd(1000)
        turtle.left(90)
        turtle.fd(600)
        turtle.left(90)
    

make_frame()


def make_sea():
    turtle.pencolor("#5A558B")
    turtle.pensize(5)
    turtle.penup()
    turtle.setpos(-490,-100)
    turtle.color("#564BC9")
    turtle.begin_fill()
    turtle.pendown()
    turtle.fd(980)
    turtle.penup()
    turtle.left(90)
    turtle.fd(150)
    turtle.left(90)
    turtle.pendown()
    turtle.fd(980)
    turtle.end_fill()


make_sea()


def make_sun():
    turtle.penup()
    turtle.setpos(-150,50)
    turtle.pendown()
    turtle.setheading(75)
    turtle.color("#D14D00")
    turtle.begin_fill()
    turtle.circle(-100,150)
    turtle.end_fill()

      
    turtle.penup()
    turtle.setpos(-170,50)
    turtle.pendown()
    turtle.setheading(75)
    turtle.color("#DF9C0C")
    turtle.begin_fill()
    turtle.circle(-170,150)
    turtle.end_fill()


    turtle.penup()
    turtle.setpos(-160,50)
    turtle.pendown()
    turtle.setheading(75)
    turtle.color("#DE7804")
    turtle.begin_fill()
    turtle.circle(-130,150)
    turtle.end_fill()


def draw_sky():
    turtle.color("#EBD98A")
    turtle.penup()
    turtle.setpos(-490,50)
    turtle.pendown()
    turtle.setheading(0)
    turtle.begin_fill()
    turtle.fd(980)
    turtle.left(90)
    turtle.fd(240)
    turtle.left(90)
    turtle.fd(980)
    turtle.left(90)
    turtle.fd(240)
    turtle.end_fill()

  

def draw_cload():
   turtle.penup()
   x = -300
   y = 200
   turtle.setpos(x,y)
   turtle.pensize(3)
   turtle.pendown()
   turtle.color("#FF9A48")
   turtle.begin_fill()
   turtle.setheading(0)
   for i in range(90):
        x+=random.randint(5,12)
        y +=random.randint(-5,5)
        turtle.setpos(x,y)
   turtle.setpos(-300,200)
   turtle.end_fill()


   
   turtle.penup()
   x = -400
   y = 100
   turtle.setpos(x,y)
   turtle.pensize(3)
   turtle.pendown()
   turtle.color("#E2AD82")
   turtle.begin_fill()
   turtle.setheading(0)
   for i in range(90):
        x+=random.randint(5,13)
        y +=random.randint(-6,6)
        turtle.setpos(x,y)
   turtle.setpos(-400,100)
   turtle.end_fill()


   turtle.penup()
   x = -400
   y = 90
   turtle.setpos(x,y)
   turtle.pensize(3)
   turtle.pendown()
   turtle.color("#E6B751")
   turtle.begin_fill()
   turtle.setheading(0)
   for i in range(90):
        x+=random.randint(5,13)
        y +=random.randint(-6,6)
        turtle.setpos(x,y)
   turtle.setpos(-400,90)
   turtle.end_fill()


   turtle.penup()
   x = -450
   y = 250
   turtle.setpos(x,y)
   turtle.pensize(3)
   turtle.pendown()
   turtle.color("#EEB947")
   turtle.begin_fill()
   turtle.setheading(0)
   for i in range(90):
        x+=random.randint(5,13)
        y +=random.randint(-6,6)
        turtle.setpos(x,y)
   turtle.setpos(-450,250)
   turtle.end_fill()


def draw_beach():
    
    turtle.penup()
    turtle.setpos(-490,-290)
    turtle.pendown()
    turtle.setheading(0)
    turtle.color("#967F4E")
    turtle.begin_fill()
    turtle.fd(980)
    turtle.left(90)
    turtle.fd(240)
    turtle.left(90)
    turtle.fd(980)
    turtle.left(90)
    turtle.fd(240)
    turtle.end_fill()
    colors = "#422E03","#C5A806","#C99300","#C9A11D","#E08906","#EEC40B","#70470A"
    for i in range(2000):
        x = random.randint(-430,480)
        y = random.randint(-290,-110)
        a = random.randint(80,150)
        turtle.pencolor(random.choice(colors))
        turtle.pensize(2)
        turtle.penup()
        turtle.setpos(x,y)
        turtle.setheading(a)
        turtle.pendown()
        turtle.fd(100)


def draw_tree(l,a,s):
    if l>30 and s>0:
        turtle.pencolor("#2E2003")
        turtle.pensize(s)
        turtle.fd(l)
        turtle.left(a)
        draw_tree(l*0.9,a,s-2)
        turtle.right(2*a)
        draw_tree(l*0.9,a,s-2)
        turtle.left(a)
        turtle.backward(l)


def draw_leaf():
    colors = "#E74809","#D86D09","#6B520D","#FA0101"
    
    for i in range(200):
        leaf = turtle.Turtle()
        leaf.penup()
        leaf.shape("triangle")
        leaf.color(random.choice(colors))
        leaf.shapesize(0.3)
        x = random.randint(0,450)
        y = random.randint(-250,150)
        leaf.setpos(x,y)


def draw_bird():
    for i in range(7):
        l =random.randint(10,40)
        x = random.randint(-400,0)
        y = random.randint(100,200)
        turtle.penup()
        turtle.setpos(x,y)
        turtle.pencolor("black")
        turtle.pensize(3)
        turtle.pendown()
        turtle.setheading(90)
        turtle.left(50)
        turtle.fd(l)
        turtle.backward(l)
        turtle.right(100)
        turtle.fd(l)


draw_sky()
draw_cload()
make_sun()
draw_beach()
draw_leaf()
draw_bird()
for i in range(4):
    x = random.randint(150,300)
    y = random.randint(-280,-100)
    l = random.randint(50,70)
    a = random.randint(18,25)
    turtle.penup()
    turtle.setpos(x,y)
    turtle.pendown()
    turtle.setheading(90)
    draw_tree(l,a,13)

turtle.update()
turtle.done()


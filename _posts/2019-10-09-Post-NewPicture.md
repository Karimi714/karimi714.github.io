---
layout: posts
title: See MY Project
---
## This is my painting with python
the picture is:
- my painting with the turtle library of python
-
-
-




![my painting](../assets/images/my_painting.jpg "painting")

---


**توضیخات کد**:

طرح کلی نقاشی داخل یک فریم کشیده شده است. ساخت فریم با دستورات fd و تغییر زاویه در تابع رسم شده که در نهایت فریم به شکل یک مستطیل در امده است.
نقاشی غروب ساحل شامل بخش های مختلفی از جمه علفزار، درخت ها، خورشید، ابرها، پرندگان و دریا است.
 اسمان، دریا و ساحل به کمک رسم مستطیل هایی به ابعاد مشخص و رنگ امیزی انها با دستور fillرسم شده اند.
 علفزار مجموعه از خطوط رندوم است که با زاویه های رندوم اما در حدود عمودی رسم شده
درخت ها با کمک تابع هایی بازگشتی رسم شده اند که در انها زاویه ها و طول شاخه ها به طور رندوم متغیر است. مکان درخت ها در محدوده ای مشخص به طور رندوم تغییر میکند اما چون محدوده گوشه سمت راست است، همواره درخت ها نزدیک به یکدیگر هستند.
خورشید در حال غروب، از سه لایه با رنگ های نزدیک به هم و اتشین تشکیل شده است. رسم خورشید با کمک رسم نیم دایره در مکان مشخص است. با تغییر شعاع نیم دایره ها لایه های مختلف خورشید ایجاد می شوند.
برای رسم هرکدام از ابرها نقطه شروع منحصر به فردی تعیین شده. حالت توده ای ابر با تغییر طول حرکت افقی و عمودی به صورت رندوم اما در بازه محدود ایجاد شده. قلم پس از ترسیم خطوط نا متقارن ابر به نقطه شروع باز می گردد و داخل ابر را رنگ میکند.
پرنده ها از دوخط ساده و زاویه ای بین این دو خط تشکیل شده اند که در محدوده ای نزدیک به خورشیدبه صورت رندوم قرار میگیرند.
برگ های درختان مثلث هایی کوچک با رنگ های رندوم اتشین هستند که در محدوده درختان قرار گرفته اند و حالت ریزش برگ های پاییزی را ایجاد می کنند.
برای رنگ امیزی از کد های رنگی استفاده شده تا رنگ ها بیشتر حالت پاستلی و کمرنگ داشته باشندوحالت پاییزی بگیرند.
برای اینکه بخش هایی از نقاشی رنگ های رندوم اما نزدیک به هم بگیرند متغیری به اسم colors تعریف شده و محدوده رنگ های مطلوب به ان نسبت داده شده تا رنگ ها به صورت رندوم از مجموعه مورد نظر انتخاب شوند.

امیدوارم از تماشای این نقاشی لذت برده باشید.
سپاسگزار از شما بابت مطالعه توضیحات
**The Code**:
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


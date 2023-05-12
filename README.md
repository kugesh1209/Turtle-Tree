# Turtle-Tree
python source code for turtle


import turtle
from turtle import *
import colorsys
from colorsys import *
tracer(10)
bgcolor('black')
ht()

def slanted_tree(X,Y,length,direction):
    if length < 7: return
    color(hsv_to_rgb(length,1,1))
    up()
    goto(X,Y)
    down()
    seth(direction)
    pensize(length/10)
    fd(length)
    px, py= xcor(), ycor()
    slanted_tree(px,py,length* 0.75,direction +45)
    slanted_tree(px,py,length * 0.75,direction -15)
slanted_tree(100, -500, 230,90)
done()

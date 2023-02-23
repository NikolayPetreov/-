# -
from tkinter import *
from random import *

def change_1():
  x = randint(0, 900)
  y = randint(0, 900)
  z = randint(0, 900)
  w = randint(0, 900)
  r = randint(0, 900)
  e = randint(0, 900)
  f = randint(1, 4)
  lst = ['red', 'blue', 'green', 'black,', 'brown', 'pink', 'purple']
  t = choice(lst)
  if f == 1:
    canvas.create_rectangle(x, y, z, w, fill=t)
  elif f == 2:
    canvas.create_polygon(x, y, z, w, r, e, fill=t)
  elif f == 3:
    canvas.create_oval(x, y, z, w, fill=t)

window = Tk()
canvas = Canvas(window, width= 1000, height = 900, bg = 'white')
canvas.pack()

Button(text='запуск', command=change_1).pack()

canvas.delete("all")

window.mainloop()

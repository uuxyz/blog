---
title: "Python modules"
date: 2022-10-16T00:51:10+08:00
draft: true
---

## python

```python
print(x)
input([prompt])
int(object)
float(object)
abs(x)
help()
len(seq)
str(x)
chr(x)
ord(x)
round(x[,n])
max(s,[,args...])
min(s,[,args...])
```

## turtle

```python
import turtle
n=int(input("n:"))
a=int(input("a:"))
d=(n-2)*180/n
t=turtle.Pen()
for i in range(n):
    t.forward(a)
    t.left(180-d)
turtle.done()
```

## math

```python
math.e
math.pi
math.ceil(x)
math.floor(x)
math.pow(x,y)
math.log(x)
math.sin(x)
math.cos(x)
math.tan(x)
math.degrees(x)
math.radians(x)
```

## random

```python
random.random()     # [0,1)
random.uniform(a,b) # [a,b]
random.randint(a,b) # [a,b]
random.choice(seq)
random.sample(seq,k)
random.shuffle(seq)
```

## PIL.Image

```python
from PIL import Image
im = Image.open("school.jpg")
print(im.format)
print(im.size)
print(im.mode)
im.rotate(45).show()
```

## numpy

```python
import numpy as np
```

## matplotlib.pyplot

```python
import matplotlib.pyplot as plt
```

```python
from PIL import Image
import numpy as np
import matplotlib.pyplot as plt
img=np.array(Image.open("lena.jpg").convert("L"))
rows,cols = img.shape
for i in range(rows):
    for j in range(cols):
        if (img[i,j]>128):
            img[i,j]=1
        else:
            img[i,j]=0
plt.figure("lena")
plt.imshow(img,cmap="gray")
plt.axis("off")
plt.show()
```

## file

```python
f = open("test.txt","r")
f.read()
for line in f.readlines():
    print(line.strip())
f.write("Hello")
f.close()

#    'r'       open for reading (default)
#    'w'       open for writing, truncating the file first
#    'x'       create a new file and open it for writing
#    'a'       open for writing, appending to the end of the file if it exists
#    'b'       binary mode
#    't'       text mode (default)
#    '+'       open a disk file for updating (reading and writing)
#    'U'       universal newline mode (deprecated)

from PIL import Image
x_start = 12               # 起始点坐标
y_start = 92
fill_width   = 24          # 信息点宽度
fill_height  = 12          # 信息点高度
space_width  = 16          # 间隔宽度
space_height = 15          # 间隔高度
num_length = 9             # 准考证号长度

def bw_judge(R, G, B):     # bw_judge用于判断一个像素的填涂情况
    Gray_scale = 0.299 * R + 0.587 * G + 0.114 * B
    return Gray_scale < 132

def fill_judge(x, y):      # fill_judge用于判断信息点的填涂情况
    count = 0
    for i in range(x, x + fill_width + 1):
        for j in range(y, y + fill_height + 1):
            R, G, B = pixels[i, j]
            if bw_judge(R, G, B) == True:
                count = count + 1
    if count >= fill_width * fill_height * 0.64:
        return True

total_width  = fill_width + space_width
total_height = fill_height + space_height
image = Image.open("fill.bmp")
pixels = image.load()
number = ""

for col in range(num_length):         # x从左至右，y从上至下对填涂区进行检测
    for row in range(10):
        x = x_start + total_width  * col
        y = y_start + total_height * row
        if fill_judge(x, y) == True:
            number = number + str(row)
            break
    else:                            # 10个信息点检测完毕后未发现有填涂
        number = number + '#'
print(number)

```

## pandas

```python

```

## os

```python

```

## wordcloud

```python

```

## jieba

```python

```

## microbit

```python

```

## serial

```python

```

## flask

```python

```

## json

```python

```

## sqlite3

```python

```

## datetime

```python

```

## Obloq

```python

```

---
title: "Code in ncee"
date: 2022-10-27T01:37:02+08:00
draft: false
---

# 必修1  数据与计算

## 必修1 第一章 素材

## 必修1 第二章 素材

## 必修1 第三章 素材

### 3.1 用计算机解决问题的一般过程

```python
import turtle
n=int(input("请输入正多边形的边数n："))
a=int(input("请输入边长a："))
d=(n-2)*180/n
t=turtle.Pen()
for i in range(n):          #重复执行n遍
    t.forward(a)            #向前绘制长度为a的线段
    t.left(180-d)           #向左旋转（180-d）度
```

### 3.2 Python语言程序设计

#### 3.2 实践与体验——编程实现图像的简单处理

```python
from PIL import Image
import numpy as np
import matplotlib.pyplot as plt
img=np.array(Image.open('lena.jpg').convert('L'))
rows,cols=img.shape
for i in range(rows):
    for j in range(cols):
        if (img[i,j]<=128):
            img[i,j]=0
        else:
            img[i,j]=1
plt.figure("lena ")
plt.imshow(img,cmap='gray')
plt.axis('off')
plt.show()
```

### 3.3 简单算法及其程序实现

#### 3.3 实践与体验——图像字符画

```python
from PIL import Image
serarr=['@','#','$','%','&','?','*','o','/','{','[','(','|','!','^','~','-','_',':',';',',','.','`',' ']
count=len(serarr)

def toText(image_file):
   asd =''                                      # 储存字符串
   for h in range(0,  image_file.size[1]):      # 垂直方向
      for w in range(0, image_file.size[0]):    # 水平方向
         r,g,b =image_file.getpixel((w,h))
         gray =int(r* 0.299+g* 0.587+b* 0.114)
         asd=asd+serarr[int(gray/(255/(count-1)))]
      asd=asd+'\r\n'
   return asd

image_file = Image.open("boy.jpg")              # 打开图片
image_file=image_file.resize((int(image_file.size[0]*0.9), int(image_file.size[1]*0.5)))   #调整图片大小

tmp=open('boy.txt','a')
tmp.write(toText(image_file))
tmp.close()
```

#### 使用Image模块实现填涂判断

```python
def bw_judge(R,G,B):
    Gray_scale=0.299*R+0.587*G+0.114*B
    if Gray_scale<132:
        color="黑色"
    else:
        color="白色"
    return color

from PIL import Image
im = Image.open("RGB.bmp")
pix = im.load()
width = im.size[0]                        # size中有两个参数，第1个参数为图像宽度值
height = im.size[1]                       # 第2个参数为图像高度值
count=0
for x in range(width):
    for y in range(height):
        R,G,B = pix[x, y]                 # 根据像素坐标获得该点的 RGB 值
        if bw_judge(R,G,B)=="黑色":       # bw_ judge函数用于判断黑、白像素
            count=count+1
if count>=width*height*0.64:
    print("已填涂！")
else:
    print("未填涂！")
```


#### 准考证号填涂识别
```python
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

#### 判定黑白像素
```python
R=43
G=10
B=241
Gray_scale=0.299*R+0.587*G+0.114*B
if Gray_scale<132:
    print('黑色')
else:
    print('白色')
```

#### 统计5个像素中的黑色像素个数
```python
count=0
Gray_scale=[47,178,146,185,116]
for i in range(0,len(Gray_scale)):
    if Gray_scale[i]<132:
        print("第"+str(i+1)+"个像素为黑色；")
        count=count+1
print("黑色像素总共有："+str(count)+"个。")
```

#### 读取文件数据实现填涂判断
```python
fname = input('Your text file name here: ')
f = open(fname,'r+')           # 以读写的方式打开文件
count=0

line = f.readline()            # 从文件中读取一行
while line:                    # 当line非空（从文件读取到了数据）
    line = line.split()        # 把空白字符去除，变成包含三个str的list
    R, G, B = map(int, line)   # 把line中三个str转化成int并赋值给R, G, B
    if 0.299 * R + 0.587 * G + 0.144 * B < 132:
        count = count + 1
    line = f.readline()        # 继续读取一行

if count >= 300 * 0.64:
    f.write("\n已填涂！")
else:
    f.write("\n未填涂！")
f.close()
```

## 必修1 第四章 素材

### 4.2 身边的百家姓
```python
# -*- coding: utf-8 -*-

import pandas as pd
#import numpy  as np
import matplotlib.pyplot as plt

#显示中文字体处理需要
from matplotlib.font_manager import FontProperties

# 读文件
df = pd.read_csv('names.csv')

# 增加2列，存放 姓、名

df['xing']=''
df['ming']=''

# 定义复姓 list
fx=['欧阳','太史','端木','上官','司马','东方','独孤','南宫','万俟','闻人','夏侯','诸葛','尉迟','公羊',
'赫连','澹台','皇甫','宗政','濮阳','公冶','太叔','申屠','公孙','慕容','仲孙','钟离','长孙','宇文',
'司徒','鲜于','司空','闾丘','子车','亓官','司寇','巫马','公西','颛孙','壤驷','公良','漆雕','乐正',
'宰父','谷梁','拓跋','夹谷','轩辕','令狐','段干','百里','呼延','东郭','南门','羊舌','微生','公户',
'公玉','公仪','梁丘','公仲','公上','公门','公山','公坚','左丘','公伯','西门','公祖','第五','公乘'
]

# 取姓、名
j=0
for i in df['xm']:
    # 不是复姓
    df['xing'][j]=i[0:1]
    df['ming'][j]=i[1:]

    #复姓处理
    if i[0:2] in fx:
        df['xing'][j]=i[0:2]
        df['ming'][j]=i[2:]

    j=j+1

# 分组计数
s= df.groupby('xing').count()

# sort 排序   结果
#s=s.sort('xm')
s=s.sort_values('xm',ascending=False)

#前20绘图
ax=s[0:20].plot(kind='bar',rot=0)

#显示中文标签
#font = FontProperties(fname=r"c:\windows\fonts\simsun.ttc", size=14)
#for label in ax.get_xticklabels() :
#    label.set_fontproperties(font)

#显示图形
#plt.show()
df.bar
```

### 4.2 实践与体验 中文分词与标签云

### 巩固提高 4.选课python
```python
# -*- coding: utf-8 -*-
"""
@author: hehy 7选3统计
"""

import pandas as pd
import itertools

#读数据到 Pandas的DataFrame 结构中
df=pd.read_csv("xk73.csv",sep=',',header='infer',encoding='utf-8')
km=['物理','化学','生物','政治','历史','地理','技术']
zrs=len(df.index)   #总人数

#按学校分组计数
sc=df.groupby('学校代码',as_index=False).count()
# 对分组计数结果进行合计，合计结果转换为DF结构并转置为行
df_sum=pd.DataFrame(data=sc.sum()).T
df_sum['学校代码']='合计'

# 增加“合计"行
result = sc.append(df_sum)

# 百分比计算
df_percent = df_sum
df_percent['学校代码']='比例'
for k in km:
    per = df_percent.at[0,k]/zrs
    df_percent[k]=per

# 增加“百分比”行
result = result.append(df_percent)

 #删除“姓名”列
result =result.drop('姓名',axis=1)
#修改“学生编号”为“总人数”
result = result.rename(columns={'学生编号':'总人数'})

#保存结果
result.to_excel("学校人数统计.xlsx")
```

## 必修1 第五章 素材

# 必修2  信息系统与社会

## 必修2 第一章

## 必修2 第二章

### 2.4 实践与体验

```python
from microbit import *
while True:
    if uart.any():
        incoming = str(uart.readall(), "UTF-8")
        incoming=incoming.strip('\r')
        if incoming=='H':
            display.show(Image.HAPPY)
            print("I am happy")
        elif incoming=='S':
            display.show(Image.SAD)
            print("I am sad")
        else:
            print("err")
```

```python
import serial
ser = serial.Serial()
ser.baudrate = 115200
ser.port = 'COM3'
ser.open()
```

```python
import serial,time
ser = serial.Serial()
ser.baudrate = 115200
ser.port = 'COM3'
ser.open()
while True:
    time.sleep(1)
    ser.write('H'.encode())
    time.sleep(1)
    ser.write('S'.encode())
```

```python
import serial,time
ser = serial.Serial()
ser.baudrate = 115200
ser.port = 'COM3'
ser.open()
while True:
    name=input()
    ser.write(name.encode())
    line = ser.readline()
    print(line.strip().decode())
```

### 2.4.3 传感器信息的获取

```python
from microbit import *
while True:
    print(temperature())
    sleep(200)
```

```python
import serial
ser = serial.Serial()
#设置通讯波特率，需要与micro:bit中设定的通讯速率一致
ser.baudrate = 115200
#设置串口号
ser.port = 'COM3'
ser.open()
while True:
    print(ser.readline())
```

```python
import serial
ser = serial.Serial()
ser.baudrate = 115200
ser.port = 'COM3'
ser.open()
f= open('microbit.txt', 'wb')
#读取20行的数据
a=20
while a>0:
	a-=1
    line=ser.readline()
	print(line)
	f.write(line)
f.close()
ser.close()
```

### 2.6.3 编写网络应用程序

```python
from flask import Flask
from flask_script import Server,Manager

app = Flask(__name__)
manager = Manager(app)
server = Server(host="0.0.0.0",port=80,threaded=True)
manager.add_command("runserver",server)

@app.route('/')
def index():
    return '这是我的第一个网页程序！'

if __name__ == '__main__':
    manager.run()
```

```python
from flask import Flask, render_template
from flask_script import Server, Manager
from flask_bootstrap import Bootstrap
from flask_moment import Moment
from flask_wtf import FlaskForm
from wtforms import StringField, SubmitField
from wtforms.validators import Required

import sys
sys.path.insert(0, "../")

import aiml
k = aiml.Kernel()
k.learn("cn-startup.xml")
k.respond("load aiml cn")
k.respond("start")

app = Flask(__name__)
app.config['SECRET_KEY'] = 'hard to guess string'

manager = Manager(app)
server = Server(host="127.0.0.1", port=80, threaded=True)
manager.add_command("runserver", server)
bootstrap = Bootstrap(app)
moment = Moment(app)

class NameForm(FlaskForm):
    name = StringField('请开始交谈：', validators=[Required()])
    submit = SubmitField('提交')

@app.route('/', methods=['GET', 'POST'])
def index():
    name = ''
    form = NameForm()
    if form.validate_on_submit():
        name = form.name.data
        form.name.data = ''
    return render_template('index.html', form=form, name=k.respond(name))

if __name__ == '__main__':
    manager.run()
```

### 2.6.4 调试发布

```python
import os
from flask import Flask
from flask_script import Server, Manager
from flask_sqlalchemy import SQLAlchemy
#导入数据库支持模块SQLAlchemy

basedir = os.path.abspath(os.path.dirname(__file__))   #获取应用程序路径

app = Flask(__name__)
app.config['SQLALCHEMY_DATABASE_URI'] =\
    'sqlite:///' + os.path.join(basedir, 'db\\tlkDB.db')
#设置数据库为运行文件目录下的db\tlkDB.db
app.config['SQLALCHEMY_COMMIT_ON_TEARDOWN'] = True

manager = Manager(app)
server = Server(host="0.0.0.0", port=80, threaded=True)
manager.add_command("runserver", server)
db = SQLAlchemy(app) #建立应用app的数据库对象db

#定义表tlkTxt的模型CltkTxt，在Python代码中CltkTxt就代表tlkTxt表。
class CtlkTxt(db.Model):
    __tablename__ = 'tlkTxt'
    id = db.Column(db.Integer, primary_key=True, index=True)
    own = db.Column(db.Integer)
    txt = db.Column(db.String(256))

    def __repr__(self):
        return '<CtlkTxt %r>' % self.txt

if __name__ == '__main__':
    db.create_all()      #创建数据库db\tlkDB.db
    manager.run()
```

```python
#SSH，再次测试SSH
import os
from flask import Flask, render_template, session, redirect, url_for, flash
#from flask_debugtoolbar import DebugToolbarExtension
from flask_script import Server, Manager
from flask_bootstrap import Bootstrap
from flask_moment import Moment
from flask_wtf import FlaskForm
from wtforms import StringField, SubmitField
from wtforms.validators import Required
from flask_sqlalchemy import SQLAlchemy

import sys
sys.path.insert(0, "../")

import aiml

k = aiml.Kernel()
k.learn("cn-startup.xml")
k.respond("load aiml cn")
k.respond("start")

basedir = os.path.abspath(os.path.dirname(__file__))

app = Flask(__name__)
app.config['SECRET_KEY'] = '<replace with a secret key>'
app.config['SQLALCHEMY_DATABASE_URI'] = \
    'sqlite:///' + os.path.join(basedir, 'db\\tlkDB.db')
app.config['SQLALCHEMY_COMMIT_ON_TEARDOWN'] = True
app.config['SQLALCHEMY_TRACK_MODIFICATIONS'] = True
#app.debug = True
#toolbar = DebugToolbarExtension(app)

manager = Manager(app)
#server = Server(host="0.0.0.0", port=80, use_debugger=True)
server = Server(host="0.0.0.0", port=80)
manager.add_command("runserver", server)
bootstrap = Bootstrap(app)
moment = Moment(app)
db = SQLAlchemy(app)

class CtlkTxt(db.Model):
    __tablename__ = 'tlkTxt'
    id = db.Column(db.Integer, primary_key=True, index=True)
    own = db.Column(db.Integer)
    txt = db.Column(db.String(256))

    def __repr__(self):
        return '<CtlkTxt %r>' % self.txt


class NameForm(FlaskForm):
    name = StringField('请开始交谈：', validators=[Required()])
    submit = SubmitField('提交')
#    submit1 = SubmitField('清除')


@app.errorhandler(404)
def page_not_found(e):
    return render_template('404.html'), 404

@app.errorhandler(500)
def internal_server_error(e):
    return render_template('500.html'), 500

@app.route('/', methods=['GET', 'POST'])
def index():
    name = ''
    rp_name = ''
    form = NameForm()
    if form.validate_on_submit():
        name = form.name.data
        form.name.data = ''
        rp_name = k.respond(name)
        if rp_name == "":
            rp_name = "......(沉默）"
        my_txt = CtlkTxt(own = 1, txt = name)
        robot_txt = CtlkTxt(own = 0, txt = rp_name)
        db.session.add(my_txt)
        db.session.add(robot_txt)
        db.session.commit()

    n = CtlkTxt.query.count()
    MtlkTxt = CtlkTxt.query.all()
    i = 0
    tdstr = ''
    while i<n:
        if MtlkTxt[i].own:
            whostr = "我："
            clrstr = "<font color=#ff0000>"
        else:
            whostr = "机器人："
            clrstr = "<font color=#0000ff>"
        tdstr = tdstr + clrstr + whostr + MtlkTxt[i].txt + "</font><br />"
        i = i+1

    return render_template('index.html', tdstr=tdstr, form=form, name=rp_name)

#@app.route('/')
#def index():
#    return render_template('index.html')


#@app.route('/talk/<word>')
#def talk(word):
#    return render_template('user.html', webword=k.respond(word))


if __name__ == '__main__':
    manager.run()
#    app.run()
#    app.run(debug=True)
```

## 必修2 第三章

### 3.2  凯撒密码加解密

```python
def  change(code,key):
    code= code.lower()
    m = ord(code)
    if m >= 97 and m <= 122:
        m = 97 + ((m - 97) + key) % 26
    return chr(m)

def  encrypt(code,key):
    code_new =""
    for s in code:
        code_new += change(s,key)
    print(code_new)
    return code_new

def  decrypt(code,key):
    code_new =""
    for s in code:
        m=ord(s)
        code_new +=chr(m-key)
    print(code_new)
    return code_new

def main():
    print("请选择数字1或2：")
    print("1：加密")
    print("2：解密")
    select = input()
    if select == "1":
        code = input("请输入加密字符串：")
        key = int(input("请输入偏移位数："))
        encrypt(code,key)
    elif select == "2":
        code = input("请输入解密字符串：")
        key = int(input("请输入偏移位数："))
        decrypt(code,key)
    else:
        print("输入错误，请重试！")

if __name__ == '__main__':
    main()
```

### 3.2  巩固与提高  简单异或

```python
def encrypt(code, key):
  code_new = ""
  for i in range(len(code)):
    code_new += str(int(code[i]) ^ int(key[i]))
  print(code_new)
  return code_new
def main():
    code = input("请输入加密字符串：")
    key =input("请输入密钥字符串：")
    encrypt(code,key)
if __name__=='__main__':
    main()
```

### 3.2  思考与练习  换位密码

```python
def encrypt(code, key):
    code_new = ""
    for i in range(len(code)):
        code_new += code[(i+key)%len(code)]
    print(code_new)
    return code_new
def main():
    code = input("请输入加密字符串：")
    key = int(input("请输入偏移位数："))
    encrypt(code,key)
if __name__=='__main__':
   main()
```

## 必修2 第四章

### get_json（项目挑战-数据可视化）
```python
#读取传感器编号为1的json数据，并绘图
import sys, urllib.request, json
import pandas as pd
import matplotlib.pyplot as plt
url = 'http://127.0.0.1:8080/get?id=1'
req = urllib.request.Request(url)
resp = urllib.request.urlopen(req)
content = resp.read().decode('utf-8')
#content=open('new-json.txt').read()
if (content):
    #print(content)
    data = json.loads(content)
    #节点可以这样读出
    print(data['sensorid'])
    val=data["value"]
    print(val[0])
    df=pd.DataFrame(val)
    #print(df)
    #绘图，默认是折线图
    ax=df.plot()
    #显示图形
    plt.show()
```

### iot-microbit（dh11）
```python
from microbit import *
import Obloq
import dht11
#DH11接在pin16

IP="192.168.43.184"
PORT="8080"
SSID="jf"
PASSWORD="20040404"

uart.init(baudrate=115200, bits=8, parity=None, stop=1, tx=pin2, rx=pin1)

while Obloq.connectWifi(SSID,PASSWORD,10000) != True:
  display.show(".")

display.scroll(Obloq.ifconfig())
Obloq.httpSet(IP,PORT)

while True:
  temp,hum=dht11.read(16)
  errno,resp=Obloq.get("input?id=1&val="+str(temp),10000)
  if errno == 200:
    display.scroll(resp)
  else:
    display.scroll(str(errno))
  sleep(1000*5)
```

### iot-microbit（dh11-完整-提示音）
```python
from microbit import *
import Obloq
import dht11
import music
#DH11接在pin16

IP="192.168.43.184"
PORT="8080"
SSID="jf"
PASSWORD="20040404"

uart.init(baudrate=115200, bits=8, parity=None, stop=1, tx=pin2, rx=pin1)

while Obloq.connectWifi(SSID,PASSWORD,10000) != True:
  display.show(".")

display.scroll(Obloq.ifconfig())
Obloq.httpSet(IP,PORT)

while True:
  temp,hum=dht11.read(16)
  errno,resp=Obloq.get("input?id=1&val="+str(temp),10000)
  if errno == 200:
    display.scroll(resp)
    if resp="0":
      music.pitch(440, 2000)
      display.scroll("SOS")
  else:
    display.scroll(str(errno))
  sleep(1000*5)
```

### iot-microbit（dh11-完整-语音）
```python
from microbit import *
import Obloq
import dht11
import speech
#DH11接在pin16

IP="192.168.43.184"
PORT="8080"
SSID="jf"
PASSWORD="20040404"

uart.init(baudrate=115200, bits=8, parity=None, stop=1, tx=pin2, rx=pin1)

while Obloq.connectWifi(SSID,PASSWORD,10000) != True:
  display.show(".")

display.scroll(Obloq.ifconfig())
Obloq.httpSet(IP,PORT)

while True:
  temp,hum=dht11.read(16)
  errno,resp=Obloq.get("input?id=1&val="+str(temp),10000)
  if errno == 200:
    display.scroll(resp)
    if resp="0":
      speech.say("Be careful,Be careful")
      display.scroll("SOS")
  else:
    display.scroll(str(errno))
  sleep(1000*5)
```

### iot-microbit（lm35）
```python
from microbit import *
import Obloq
#Lm35接在pin0

IP="192.168.43.184"
PORT="8080"
SSID="jf"
PASSWORD="20040404"

uart.init(baudrate=115200, bits=8, parity=None, stop=1, tx=pin2, rx=pin1)

while Obloq.connectWifi(SSID,PASSWORD,10000) != True:
  display.show(".")

display.scroll(Obloq.ifconfig())
Obloq.httpSet(IP,PORT)

while True:

  errno,resp=Obloq.get("input?id=1&val="+str(pin0.read_analog()),10000)
  if errno == 200:
    display.scroll(resp)
  else:
    display.scroll(str(errno))
  sleep(1000*5)
```

### iot-microbit（自带温度）
```python
from microbit import *
import Obloq

IP="192.168.0.103"
PORT="8080"
SSID="jys16f"
PASSWORD="zjjys.16"

uart.init(baudrate=115200, bits=8, parity=None, stop=1, tx=pin2, rx=pin1)

while Obloq.connectWifi(SSID,PASSWORD,10000) != True:
  display.show(".")

display.scroll(Obloq.ifconfig())
Obloq.httpSet(IP,PORT)

while True:

  errno,resp=Obloq.get("input?id=1&val="+str(temperature()),10000)
  if errno == 200:
    display.scroll(resp)
  else:
    display.scroll(str(errno))
  sleep(1000*5)
```

# 选择性必修1 数据与数据结构

## 2.1 数组

```python
from random import randint
a=[0]*20
b=[0]*15
c=[0]*35
a[0]=randint(95, 100)
for i in range(1,20):
    a[i]=a[i-1]-randint(1, 5)
b[0]=randint(95, 100)
for i in range(1,15):
    b[i]=b[i-1]-randint(1, 5)
print("原始数据序列一为：")
print(a)
print("原始数据序列二为：")
print(b)
i=0
j=0
k=0
while(i<20 and j<15):
    if a[i]>=b[j]:
        c[k]=a[i]
        i=i+1
        k=k+1
    else:
        c[k]=b[j]
        j=j+1
        k=k+1
while i<20:
    c[k]=a[i]
    i=i+1
    k=k+1
while j<15:
    c[k]=b[j]
    j=j+1
    k=k+1
print("合并后的数据序列为：")
print(c)
```

```python
from random import randint
a=[[100-4*i+randint(-1,1),i+1] for i in range(0,15)]
b=[[100-4*i+randint(-1,1),i+1] for i in range(0,20)]
a[-1][-1]=b[-1][-1]=-1
ptr_a=ptr_b=0
while ptr_b!=-1:
    while a[ptr_a][0]>b[ptr_b][0] and a[ptr_a][1]!=-1:
        ptr_a=a[ptr_a][1]
    if a[ptr_a][0]<=b[ptr_b][0]:
        a[ptr_a][0],b[ptr_b][0]=b[ptr_b][0],a[ptr_a][0]
    a.append([b[ptr_b][0],a[ptr_a][1]])
    a[ptr_a][1]=len(a)-1
    ptr_b=b[ptr_b][1]
ptr_c=0
while ptr_c!=-1:
    print(a[ptr_c][0],end=" ")
    ptr_c=a[ptr_c][1]
```

## 2.2 链表

```python
from random import randint
data_a=[]
head_a=-1
data_b=[]
head_b=-1
tmp=randint(95, 100)
data_a.append([tmp,head_a])
head_a=0
for i in range(1,20):
    tmp=data_a[i-1][0]-randint(1, 5)
    data_a.append([tmp,data_a[i-1][1]])
    data_a[i-1][1]=i
print("链表结构的原始数据序列一")
print(data_a)
tmp=randint(95, 100)
data_b.append([tmp,head_b])
head_b=0
for i in range(1,25):
    tmp=data_b[i-1][0]-randint(1, 5)
    data_b.append([tmp,data_b[i-1][1]])
    data_b[i-1][1]=i
print("链表结构的原始数据序列二")
print(data_b)
k_a=head_a
q_a=head_a
k_b=head_b
while (k_a!=-1 and k_b!=-1):
    if data_a[k_a][0]>=data_b[k_b][0]:
        q_a=k_a
        k_a=data_a[k_a][1]
    else:
        if k_a==head_a:
            data_a.append([data_b[k_b][0],head_a])
            head_a=len(data_a)-1
            q_a=head_a
            k_b=data_b[k_b][1]
        else:
            data_a.append([data_b[k_b][0],k_a])
            data_a[q_a][1]=len(data_a)-1
            q_a=data_a[q_a][1]
            k_b=data_b[k_b][1]
while k_b!=-1:
    data_a.append([data_b[k_b][0],-1])
    data_a[q_a][1]=len(data_a)-1
    q_a=data_a[q_a][1]
    k_b=data_b[k_b][1]
print("链表结构合并后数据序列")
print(data_a)
print("按链表链接顺序输出数据序列")
tmp=head_a
while data_a[tmp][1]!=-1:
    print(data_a[tmp][0],end=" ")
    tmp=data_a[tmp][1]
print(data_a[tmp][0])
```

```python
llist=[]
n=int(input("请输入参与人数(N):"))
m=int(input("请输入淘汰数(M):"))
for i in range(n-1):
    llist.append([i+1,i+1])
llist.append([n,0])
head=0
long=n
k=head
i=1
while long > 1:
    i=i+1
    if i==m:
        t=llist[k][1]
        llist[k][1]=llist[t][1]
        if t==head:
            head=llist[k][1]
        i=1
        long=long-1
    k=llist[k][1]
print(llist[head][0])
```

## 3.1字符串
### 回文串
```python
s=input("请输入一个字符串:")
length=len(s)
mid=length//2
left=s[0:mid]
temp=s[-mid:]
right=""
for i in range(len(temp)):
    right=right+temp[len(temp)-i-1]
if left==right:
    print("Yes")
else:
    print("No")

s=input("请输入一个字符串:")
s1=s[::-1]
if s==s1:
    print("Yes")
else:
    print("No")
```
### 机动车违章识别系统
```python
import csv
f=open("车辆号码csv","r")
f_csv=csv.reader(f)
k=0
for row in f_csv:       #逐一枚举所有车辆信息
    k=k+1
    if k==1:
        print(row[0],"",row[1])
        continue
    car=row[0]
    name=row[1]
    w=row[3]
    week="12345"
    pos=0
    for letter in car:
        if letter >='A' and letter <='Z':
            if letter == 'B':
                pos=1
            break
    if pos ==0 and w!=6 and w!=7:
        print(car," ",name)
    if pos==1:
        i=len(car)
        while i>=0:
            i=i-1
            ch=car[i]
            if ch>='0' and ch<='9':
                break
        num=int(ch)
        if i<0:
            continue
        elif num==0:
            t=week[4]
        elif num<=5:
            t=week[int(ch)-1]
        else:
            t=week[9-int(ch)]
        if t==w:
            print(car," ",name)
f.close()
```
### 正则表达式
```python
def findphone(text):
    for i in range(0, len(text)):
        flag=True
        if text[i].isdecimal() and i<len(text)-12:
            for j in range(i+1, i+4):
                if not text[j].isdecimal():         #判断是否为数字 
                    flag=False
            if text[i+4]!='-':
                flag=False
            for j in range(i+5, i+13):
                if not text[j].isdecimal():
                    flag=False
            if flag:
                return text[i:i+13]
    else:
        return False
x=input("请输入一串字符")
result=findphone(x)
if result==False:
    print("没有找到电话号码")
else:
    print("电话号码为：",result)
```

```python
import re
phone=re.compile(r'\d\d\d\d-\d\d\d\d\d\d\d\d')
x=input("请输入一串字符")
mo=phone.search(x)
if mo:
    print("电话号码为：",mo.group())
else:
    print("没有找到电话号码")
```

## 3.2 队列
### 信息的加密
```python
s= input("请输入字符串:")
print("加密后的串为:")
que=[""]*100
head=0
tail=0
for i in range(len(s)):
    que[tail]=s[i]
    tail+=1
while head<tail:
    print(que[head],end="")
    head+=1
    if head<tail:
        que[tail]=que[head]
        tail+=1
        head+=1
```

### 银行叫号排队系统
```python
que=[-1]*1000
head=0
tail=0
print("请输入具体的操作编号:")
print("1.新到顾客(取号)")
print("2.下一个顾客(叫号)")
print("3.程序结束")
x=int(input())
while x!=3:
    if x==1:
        que[tail]=que[tail]+1
        print("您当前的号码为:A%d,需要等待的人数为%d"%(tail, tail-head))
        tail=tail+1
    if x==2:
        if head==tail:
            print("对不起,没有等待的客户")
        else:
            print("请A%d号客户准备,马上将为您办理业务。"%head)
            head=head+1
    x=int(input(“请输入操作\n"))
```
## 3.3 栈
### 十进制转二进制进出栈方式
```python
st=[-1]*100
top=-1
number=int(input("请输入十进制整数:"))
while number >0:
    x=number %2
    top=top+1
    st[top]=x
    number=number//2
while top>=0:
    print(st[top],end="")
    top=top-1
```
### 括号匹配
```python
st=[-1]*100
top=-1
flag=True
s=input("请输入数学计算式:")
for i in range(len(s)):
    if s[i]=="(":
        top=top+1
        st[top]=s[i]
    elif s[i]==")":
        if top==-1:
            flag=False
            break
        else:
            top=top-1
if top>=0:
    flag=False
if flag:
    print("括号匹配")
else:
    print("括号不匹配")
```
## 3.1 行程编码
```python
import pickle
def bian(word = ''):
    new_word = ''
    renum = 0
    pre = word[0]
    for i in range(len(word)):
        if word[i] == pre:
            renum = renum + 1
            if i == len(word) - 1: new_word += str(renum)+ ' ' + pre
        elif i != len(word) - 1:
            new_word += str(renum)+ ' ' + pre + ' '
            renum = 1
            pre = word[i]
    return new_word
f=open("图像编码.txt","rb")
st=pickle.load(f)
f.close()
b1=bian(st)
f=open("行程编码.txt","wb")
pickle.dump(b1,f)
f.close()
```

## 3.1 颜色编号
```python
def readImage(filename=''):
    from PIL import Image
    im = Image.open(filename)
    im = im.convert('1')
    im_list =''
    pix = im.load()
    width = im.size[0]          # size中有两个参数，第1个为图像宽度值
    height = im.size[1]         # 第2个参数为图像高度值
    count=0
    im.show(filename)
    for x in range(width):
        for y in range(height):
            im_list += str(pix[x, y]//255)      # 根据像素点坐标获得该点的 RGB 值
    return im_list
im_list1 = readImage('黑白图片.bmp')
import pickle
#保存数据
f = open('图像编码.txt', 'wb')
pickle.dump(im_list1, f)
f.close()
```

## 五子棋
```python
n=5
qp=[[0 for i in range(n)] for j in range(n)]
for i in range(n):
    print(qp[i])
emp=n*n
f=1
long=0
while (long<5)and(emp>0):
    long=1
    if f==1:
        print("请黑方落子")
    else:
        print("请白方落子")
    x,y=input("请输入落子位置：").split(" ")
    x=int(x)
    y=int(y)
    while (x<0)or(x>=n)or(y<0)or(y>=n)or(qp[x][y]!=0):
        print("该位置不能落子，请重新输入落子位置！")
        x,y=input("请输入落子位置：").split(" ")
        x=int(x)
        y=int(y)
    if f==1:
        qp[x][y]=1
    else:
        qp[x][y]=2
    for i in range(n):
        print(qp[i])
    if f==1:
        t=1
        while (y+t<n)and(qp[x][y+t]==1):
            t=t+1
        longx=t
        t=1
        while (y-t>=0)and(qp[x][y-t]==1):
            t=t+1
        longx=longx+t-1
        if long<longx:
            long=longx
        t=1
        while (x+t<n)and(qp[x+t][y]==1):
            t=t+1
        longy=t
        t=1
        while (x-t>=0)and(qp[x-t][y]==1):
            t=t+1
        longy=longy+t-1
        if long<longy:
            long=longy
        t=1
        while (x+t<n)and(y+t<n)and(qp[x+t][y+t]==1):
            t=t+1
        longz=t
        t=1
        while (x-t>=0)and(y-t>=0)and(qp[x-t][y-t]==1):
            t=t+1
        longz=longz+t-1
        if long<longz:
            long=longz
        t=1
        while (x+t<n)and(y-t>=0)and(qp[x+t][y-t]==1):
            t=t+1
        longz=t
        t=1
        while (x-t>=0)and(y+t<n)and(qp[x-t][y+t]==1):
            t=t+1
        longz=longz+t-1
        if long<longz:
            long=longz
    else:
        t=1
        while (y+t<n)and(qp[x][y+t]==2):
            t=t+1
        longx=t
        t=1
        while (y-t>=0)and(qp[x][y-t]==2):
            t=t+1
        longx=longx+t-1
        if long<longx:
            long=longx
        t=1
        while (x+t<n)and(qp[x+t][y]==2):
            t=t+1
        longy=t
        t=1
        while (x-t>=0)and(qp[x-t][y]==2):
            t=t+1
        longy=longy+t-1
        if long<longy:
            long=longy
        t=1
        while (x+t<n)and(y+t<n)and(qp[x+t][y+t]==2):
            t=t+1
        longz=t
        t=1
        while (x-t>=0)and(y-t>=0)and(qp[x-t][y-t]==2):
            t=t+1
        longz=longz+t-1
        if long<longz:
            long=longz
        t=1
        while (x+t<n)and(y-t>=0)and(qp[x+t][y-t]==2):
            t=t+1
        longz=t
        t=1
        while (x-t>=0)and(y+t<n)and(qp[x-t][y+t]==2):
            t=t+1
        longz=longz+t-1
        if long<longz:
            long=longz
    emp=emp-1
    if (emp>0)and(long<5):
        if f==1:
            f=2
        else:
            f=1
if emp==0:
    print("游戏结束，平局！")
elif long>=5:
    if f==1:
        print("游戏结束，黑方胜！")
    else:
        print("游戏结束，白方胜！")
```

## 第三章 巩固与提高 软硬车厢
```python
#S:软
#H:硬
s=input("请输入n节软硬车厢的序列：")
stack=[""]*100
top=-1
for i in range(len(s)):
      if s[i]=="H":
            top+=1
            stack[top]=i+1
            print("第%d节车厢入栈"%(i+1))
      else:
            top+=1
            print("第%d节车厢入栈"%(i+1))
            top-=1
            print("第%d节车厢出栈"%(i+1))
while top>-1:
       print("第%d节车厢出栈"%(stack[top]))
       top-=1
```

## 第三章 巩固与提高 餐馆取号叫号
```python
queuetwo=[-1]*100
queuefour=[-1]*100
queuesix=[-1]*100
headtwo=0
tailtwo=0
headfour=0
tailfour=0
headsix=0
tailsix=0
print("请输入具体的操作：")
x=int(input())
while x!=0:
    if x==2:
        queuetwo[tailtwo]=queuetwo[tailtwo]+1
        print("您当前的号码为：TWO%d，需要等待的人数为%d"%(tailtwo,tailtwo-headtwo))
        tailtwo+=1
    if x==4:
        queuefour[tailfour]=queuefour[tailfour]+1
        print("您当前的号码为：FOUR%d，需要等待的人数为%d"%(tailfour,tailfour-headfour))
        tailfour+=1
    if x==6:
        queuesix[tailsix]=queuesix[tailsix]+1
        print("您当前的号码为：SIX%d，需要等待的人数为%d"%(tailsix,tailsix-headsix))
        tailsix+=1
    if x==12:
        if headtwo==tailtwo:
              print("对不起，没有等待的人")
        else:
              print("请TWO%d号客户准备，马上帮您安排"%(headtwo))
              headtwo+=1
    if x==14:
        if headfour==tailfour:
              print("对不起，没有等待的人")
        else:
              print("请FOUR%d号客户准备，马上帮您安排"%(headfour))
              headfour+=1
    if x==16:
        if headsix==tailsix:
              print("对不起，没有等待的人")
        else:
              print("请SIX%d号客户准备，马上帮您安排"%(headsix))
              headsix+=1
    x=int(input("请输入操作："))
```
## 4.1 树与二叉树
## 4.2 二叉树的基本操作
### 二叉树遍历的Python程序实现
```python
class Node:
    def __init__(self,value=None,left=None,right=None):
        self.value=value
        self.left=left
        self.right=right

def preTraverse(root):
    if root==None:
        return
    print(root.value)
    preTraverse(root.left)
    preTraverse(root.right)

def midTraverse(root):
    if root==None:
        return
    midTraverse(root.left)
    print(root.value)
    midTraverse(root.right)

def afterTraverse(root):
    if root==None:
        return
    afterTraverse(root.left)
    midTraverse(root.right)
    print(root.value)

if __name__=='__main__':
    root=Node('A',Node('B',Node('D'),Node('E')),Node('C',right=Node('F',Node('G'))))
    print('前序遍历')
    preTraverse(root)
    print('中序遍历')
    midTraverse(root)
    print('后序遍历')
    afterTraverse(root)
```
## 4.3 抽象数据类型

## 5.2 迭代与递归
```
a=int(input("请输入一个需要求其平方根的数："))
x=a/2
while ((abs((x+a/x)/2-x))>0.00001):
    x=(x+a/x)/2
print(a,"的平方根约为",round((x+a/x)/2,6))
```
### 欧几里得算法
```python
def gcd(m,n):
    while n!=0:
        temp=n
        n=m%n
        m=temp
    return m
```

### 汉诺塔游戏
```python
def move(n, a, b, c):
    if(n==1):
        print(a, "->",c)
        return
    move(n-1, a, c, b)
    move(1, a, b, c)
    move(n-1, b, a, c)
move(3,"A","B","C")
```
### 走迷宫
```python
maze = [[0, 0, 0, 0, 0, 0, 0, 0, 0, 0],
        [0, 1, 1, 0, 1, 1, 1, 0, 1, 0],
        [0, 1, 1, 0, 1, 1, 1, 0, 1, 0],
        [0, 1, 1, 1, 1, 0, 0, 1, 1, 0],
        [0, 1, 0, 0, 0, 1, 1, 1, 1, 0],
        [0, 1, 1, 1, 0, 1, 1, 1, 1, 0],
        [0, 1, 0, 1, 1, 1, 0, 1, 1, 0],
        [0, 1, 0, 0, 0, 1, 0, 0, 1, 0],
        [0, 0, 1, 1, 1, 1, 1, 1, 1, 0],
        [0, 0, 0, 0, 0, 0, 0, 0, 0, 0]]

def valid(maze, x, y):
    if(x >= 0 and x < len(maze) and y >= 0 and y < len(maze[0]) and maze[x][y] == 1):
        return True
    else:
        return False


def walk(maze, x, y):
    # 如果位置是迷宫的出口,
    if(x == 8 and y == 8):
        print("successful")
        return True
    if valid(maze, x, y):
        maze[x][y] = 2
        # 做标记,防止折回
        # 针对四个方向依次试探
        walk(maze, x-1, y)
        walk(maze, x, y-1)
        walk(maze, x+1, y)
        walk(maze, x, y+1)


walk(maze, 1, 1)
```
### 冒泡排序
```python
def bubble_sort(L):
    length=len(L)
    #序列长度为length,需要执行length-1遍加工
    for i in range(1,length):
        for j in range(0, length-i):
            if L[j]>L[j+1]:
                temp=L[j]
                L[j]=L[j+1]
                L[j+1]=temp
```
### 奥运排行榜
```python
import csv

#数据读入
csvFile=open("jp.csv","r")
reader=csv.reader(csvFile)
a=[]
for item in reader:
    a.append(item)
csvFile.close()
#排序
for i in range(1, len(a)-1):
    for j in range(1, len(a)-i):
        if int(a[j][3])<int(a[j+1][3]):
            temp=a[j]
            a[j]=a[j+1]
            a[j+1]=temp

#数据写入
csvFile2=open('jp2.csv', 'w', newline='')
writer=csv.writer(csvFile2, dialect='excel')
m=len(a)
for i in range(m):
    writer.writerow(a[i])
csvFile2.close()

```
## 5.4 数据查找
### 顺序查找
```python
d=[25,22,13,18,14,11,17,19]
key=18
flag=False
length=len(d)
for i in range(length):
    if d[i]==key:
        flag=True
        break
if flag==True:
    print("查找成功!")
else:
    print(“未找到")
```
```python
def seq_search(s,a):
    length=len(d)
    flag=False
    for i in range(length):
        if d[i]==key:
            flag=True
            break
    if flag==True:
        return i
    else:
        return False

d=[25,22,13,18,14,11,17,19]
key=15
result=seq_search(d,key)
print(result)
```
### 二分查找
```python
key=12
d=[6,12,15,18,22,25,28,35,46,58,60]
f=False
#和定义子数组的边界,一开始搜索的是整个数组
i=0
j=len(d)-1
while i <= j: 
    m=(i+j)//2
    if d[m] == key:
        f=True
        b=m
        break
    if key < d[m]:
        j=m-1
    else:
        i=m+1

if f==True:
    print("查找成功!第"+str(b)+"个")
else:
    print("没有找到!")
```
```python
def bsearch(s, array):
    if len(array)==0:
        print("未找到!")
        return False
    mid=(len(array)-1)//2
    if array[mid] == s:
        print("找到了!第"+str(mid+1)+"个")
        return True
    elif s < array[mid]:
        return bsearch(s, array[:mid-1])
    else:
        return bsearch(s, array[mid+1:])

key=12
d=[6,12,15,18,22,25,28,35,46,58,60]
print(bsearch(key, d))
```
### 航空公司VIP会员积分查询
```python
import csv
#数据读入
csvFlle=open("vip.csv","r")
reader=csv.reader(csvFile)
a=[]
for item in reader:
    a.append(item)
csvFlle.close()
#排序
def bubble_sort(d):
    for i in range(1, len(d)-1):
        for j in range(1, len(d)-1):
            if int(d[j][0])<int(d[j+1][0]):
                temp=d[j]
                d[j]=d[j+1]
                d[j+1]=temp

#二分查找
def bsearch(s, array):
    i=1                       		#查找范围不包含第一行数据
    j=len(array)-1
    while i <= j: 
        m=(i+j)//2
        if int(array[m][0]) == s:
            return m
        if s < int(array[m][0]):
            j=m-1
        else:
            i=m+1
    return -1						#未找到返回-1

bubble_sort(a)
key = int(input('请输入要查询的VP号:'))
m=bsearch(key, a)
if m!=-1:
    print(a[m][1],"先生/女士，您的积分为:",a[m][3])
else:
    print('找不到VP号对应的用户信息!')
```
# -Micropython-esp32-oled1306-sprite
a light sprite module for oled1306 drive by kilo

https://space.bilibili.com/87690728

How to use？  

for soft i2c:  
```python
  from sprite import *  
  display = initDisplay(8,9)  
  p1 = BinloaderFast("bg1000.bin",0,0)  
  p1.draw(display)  
  display.show()  
```
for hardware i2c:  
```python
  display = initDisplay(18,19,0)  
  p1 = BinloaderFast("bg1000.bin",0,0)  
  p1.draw(display)  
  display.show()  
```
and cropX:  
```python
  for i in range(80):  
    p1.cropX(0,i)  
    p1.cropdraw(display)  
    display.show()  
```

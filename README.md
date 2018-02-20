# Ledblee-Triones-control
Ledblee Triones bluetooth controled rgb strip 

http://cgi.ebay.com/ws/eBayISAPI.dll?ViewItemVersion&item=142322011085&view=all&tid=1485433771004
https://learn.adafruit.com/reverse-engineering-a-bluetooth-low-energy-light-bulb/control-with-bluez


## Color mode
```
pi@raspberrypi:~ $ sudo gatttool -I
[                 ][LE]> connect 34:15:13:E2:EF:58
Attempting to connect to 34:15:13:E2:EF:58
Connection successful
[34:15:13:E2:EF:58][LE]> char-write-cmd 0x0043 5600ff0000f0aa
[34:15:13:E2:EF:58][LE]> char-write-cmd 0x0043 560000ff00f0aa
[34:15:13:E2:EF:58][LE]>
```
56(11)(22)(33)(44)f0aa
1. Red
1. Green
1. Blue
1. White


## Pattern mode

```
sudo gatttool  -b 34:15:13:E2:EF:58 --char-write -a 0x0043 -n bb260544
```
bb(11)(22)44
* 1: Color mode
  * 23: Smooth color
  * 24: ???
  * 25: Smooth color
  * 26: Smooth red
  * 27: Smooth green
  * 28: Smooth blue
  * 29: Smooth yellow
  * 2a: Smooth cyan
  * 2b: Smooth purple
  * 2c: Smooth rgb white
  * 2d: r to g to b 
  * 2e: r to g to b 
  * 2f: r to g to b
  * 30: rgb strobe
  * 31: red strobe
  * 32: green strobe
  * 33: blue strobe
  * 34: strobe...
* 2: Speed

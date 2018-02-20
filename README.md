# Ledblee-Triones-control
Ledblee Triones bluetooth controled rgb strip 

http://cgi.ebay.com/ws/eBayISAPI.dll?ViewItemVersion&item=142322011085&view=all&tid=1485433771004
https://learn.adafruit.com/reverse-engineering-a-bluetooth-low-energy-light-bulb/control-with-bluez

```
pi@raspberrypi:~ $ sudo gatttool -I
[                 ][LE]> connect 34:15:13:E2:EF:58
Attempting to connect to 34:15:13:E2:EF:58
Connection successful
[34:15:13:E2:EF:58][LE]> char-write-cmd 0x0043 5600ff0000f0aa
[34:15:13:E2:EF:58][LE]> char-write-cmd 0x0043 560000ff00f0aa
[34:15:13:E2:EF:58][LE]>
```

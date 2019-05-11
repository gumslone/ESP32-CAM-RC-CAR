# ESP32-CAM-RC-CAR
Create your own surveillance bot controlled by an esp32-cam module

![photo](https://github.com/gumslone/ESP32-CAM-RC-CAR/blob/master/photo.jpg?raw=true)

![screenshot](https://github.com/gumslone/ESP32-CAM-RC-CAR/blob/master/Screenshot.png?raw=true)

this code is based on a default demo for the esp32-cam module,
I extended the web interface with buttons controlls to controll the rc-surveillance-car and the led,
I also added modifications the C code.

Parts that I've used:

4 motors (6V, 300rpm) with wheels, order link: http://ali.pub/3ck3ce

esp32-cam module, order link http://ali.pub/3ck3dr

motor driver, order link http://ali.pub/3ck3gv

some wires and usb to uart programmer like (http://ali.pub/3ck3je).

connect motor driver to pins:
12,13,14,15

this is a first working code (alpha version) i plan to improve and extend it soon, there is a fail safe stop, inplemented into the code, in case some connection issues, the car will stob after 500ms, you can change the value in the .ino file.

i have noticed that esp32-module doenst start sometimes properly when i connect power to it, so i have to disconnect the motor driver before i connect the power, without the motor driver the esp32 starts properly, after that i connect the power wire back to motor driver and everything works well, i think this depends on your power source (you could use two separate power sources for motor driver and esp32-cam module to fix this also adding some caps may fix this issue).

another issue that I have noticed is that I can't let the motors on left side rotate forward with the right side motors rotate backward and vice versa, it doesnt seem to work with esp32 cam module, but it works without it wery well, so any ideas are welcome.

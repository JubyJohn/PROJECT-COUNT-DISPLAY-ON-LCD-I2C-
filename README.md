# PROJECT COUNT DISPLAY ON LCD 16x2 I2C


## OVERVIEW
After completing microcontrollers upto Arduino while doing embedded engineer internship , I try to do implement software in hardware as a project aspects. But I failed. Later on I try to do  projects by incorporating two or more sensors with microcontroller.Here I used ESP8266 microcontroller.


## AIM
To display the count of pushing button on LCD I2C.


## COMPONENTS
1.	ESP8266 NodeMCU
2.	LCD 16x2 I2C
3.	Push Button
4.	Jumper Wire
5.	USB cable


## CONNECTION

### LCD16x2 I2C Module Pin Diagram
 
<br> VCC = power supply ---->  3V3
<br> GND = ground          ---->  GND
<br> SDA = serial data line   ---->  D2
<br> SCL = serial clock line   ---->  D1

### Push Button Pin Diagram

 
<br> S = Output     ---->  D6
<br> middle  = power supply  ---->  3V3
<br> –  = ground          ---->  GND


## PROCEDURE

<br> Step 1 : Interface ESP8266 microcontroller to Arduino IDE using port.
<br> Step 2: Interface ESP8266 microcontroller with push button and print the digital values on serial monitor.
<br> Step 3 : Interface ESP8266 microcontroller with LCD 16x2 I2C to display HI on LCD
<br> Step 4 : Interface ESP8266 microcontroller with LCD 16x2 I2C and push button by modifying both the programs.


## PROBLEMS FACED

### Error 1 -   While compiling , a error message keep showing starts with " A fatal esptool.py......." 
#### How to rectify:
(1) Make sure Board managers are  updated 
Update the board packages for ESP8266 through the Arduino IDE. Navigate to Tools > Board > Boards Manager, search for ESP8266 , and click Install or Update if there are newer versions available.
(2)  Install USB Drivers (if applicable):
If you're using a development board that requires specific USB drivers (especially for Windows), make sure these drivers are installed correctly. Check the documentation provided with your board.  
(3)  Reinstall Arduino IDE
As a last resort, if none of the above steps work, try reinstalling the Arduino IDE. Uninstall it completely, then download and install the latest version from the official Arduino website.       
(4)  Restart computer
As a last resort, if none of the above steps work, try restarting the 
system
### Error 2 -   Display cleared when nothing is done.
#### How to rectify:
- put some delay() after closing if loop in void loop.
### Error 3 -   Count numbers  keep on printing aside of "count ="
#### How to rectify:
- lcd.setCursor(c,r) function is used to print on the same column by eliminating previous count number by present count number.


## REFERENCES

LiquidcrystalI2C- library : http://easycoding.tn/index.php/resources/
LiquidcrystalI2C- code : http://easycoding.tn/tuniot/demos/code/














 
OUTPUT
C:\Users\JUBY JOHN\Desktop\Projects\prjt 1 i2c&push button\images

REFERENCES
LiquidcrystalI2C- library : http://easycoding.tn/index.php/resources/
LiquidcrystalI2C- code : http://easycoding.tn/tuniot/demos/code/

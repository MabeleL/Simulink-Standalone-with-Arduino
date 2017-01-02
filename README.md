# Simulink-Standalone-with-Arduino
This is an introduction to programming ATmega328P with simulink. It is a simple block generated on simulink to continously blink an LED and this will continue running on the chip even after disconnection from the PC.
 Ensure that you have connected the ATmega328P as shown by domiflichi at the following url:http://www.instructables.com/id/Standalone-Arduino-ATMega-chip-on-breadboard/. Connect an LED through a resistor on Pin 13.(https://todbot.com/blog/2009/05/23/arduino-chip-sticker-label/).
go to MATLAB terminal and type: supportPackageInstaller and select install from Internet. 
Select Arduino and check all the actions for both MATLAB and Simulink base products. 
Sign into Mathworks with your account to finish the installation. 
Connect the USB cable to the FTDI you are using to communicate with the ATmega chip. 
type simulink on MATLAB terminal to open up simulink. 
Find Simulink support Package for Arduino Hardware on the left pane of the simulink windows and click on it.
Press CTRL+n while on simulink window to open a new simulink window.
Double click on the Common container and select Digital Output block. Drag this block on the new simulink window.
Click on Sources on the Simulink sidepane and select Pulse Generator block. Drag this block to the simulink window having the Digital Output block
Double click on the Pulse Generator block and change the following parameters:
Pulse Type: Sample based
Time (t): Use simulation time.
Period: Change it to a value you want or leave the default value 0f 10.
Sample time: Insert a duration you want, say 0.1 or 0.2 seconds.
Click Apply and Ok.
You can drag a scope from sink to observe the Period, the pulse width and the sample time set above.
Connect the pulse generator block to the Digital Output block of Arduino.
Go to tools menu and select Run on Target Hardware -> prepare to run
Select your Arduino Hardware and select your board. Manually select your COM port too. Leave the baud rates as default (9600) and click ok
Click the Deploy to Hardware Button

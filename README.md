# Grbl_ESP32_Development_Controller
 A CNC controller to use and test Grbl_ESP32

![](http://www.buildlog.net/blog/wp-content/uploads/2018/10/20181007_153826.jpg)

This is a Grbl_ESP32 CNC Development board. This is a quick and easy way to use and test CNC on the ESP32 controller.

Grbl is a great CNC firmware that has been around for nearly a decade. It was originally designed for the Arduino UNO and basic 3 axis CNC routers, but it has been ported to other CPUs and was the basis for many other CNC and 3D printer firmwares.

The [firmware](https://github.com/bdring/Grbl_Esp32) was written using the Arduino IDE to make it as user friendly as possible. If you have experience with Arduinos, this will not be much different.

**I/O** - The ESP32 is very flexible allowing you to remap the the I/O features to alternate pins. Grbl_ESP32 is also far more flexible than Arduino Grbl for assigning pins to features. But, when you make a PCB, you force specific pins to specific features. To give some flexibility there are some shared pins. The SD Card shares pins with Mist coolant, Spindle Direction and Spindle Enable. These pins were chosen because they are very rarely used in DIY CNC. Full control of a variable speed spindle is still on a dedicated pin. If you really need the SD Card and some of those features, contact me. There are many alternative ways to do that. [See this wiki page for additional info on I/O](https://github.com/bdring/Grbl_Esp32/wiki/Setting-Up-the-I-O-Pins).

ESP32 brings the following features to small scale CNC.


- Powerful dual core processor running at 240MHz per core.
- 4MB of flash RAM
- Floating point coprocessor.
- On board Wifi.
- On Board Bluetooth.

The board has the following features.

- A very modular design - If the ESP32 or the stepper drivers get damaged, you can replace them.
- Socket for an ESP32 Dev board also known as NodeMCU 32S. Most 19 pin per side dev boards should work, just check the pins or ask me. Extra connector holes are positioned next to the NodeMCU 32S for test probing and to accommodate wider 19 pin modules.
- (3) Sockets for stepper motor drivers. These fit many types of drivers. The TI DRV8825 type is my favorite driver for this type of application. Micro-step selection jumpers are included. 
- Home/Limit switch connections for XY and Z axes. These also have R/C filters to eliminate high frequency noise from false triggering the switches.
- Control switch input connections for Feed Hold, Cycle Start, Reset and Door. These have filters as well as pullup resistors, because they are on inputs that do not have internal pullups.
- Spindle output for PWM (Speed).
- A micro SD Socket Note: Grbl senders do not support SD cards yet, but most have a manual console where the command is easily typed. The WebUI fully supports the SD Card.
- DC-DC power supply. There is a strong 3A DC-DC power supply to run the ESP32 if it is not connected to USB.

### Getting a pre assembled one.

This controller is generally available [for sale on Tindie](https://www.tindie.com/products/33366583/grbl_esp32-cnc-development-board-v35/).

### <a name="donation"></a>Donation

This project requires a lot of work and often expensive items for testing. Please consider a safe, secure and highly appreciated donation via the PayPal link below.

[![](https://www.paypalobjects.com/en_US/i/btn/btn_donateCC_LG.gif)](https://www.paypal.com/cgi-bin/webscr?cmd=_s-xclick&hosted_button_id=TKNJ9Z775VXB2)





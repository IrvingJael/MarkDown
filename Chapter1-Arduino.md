# Chapter 1: The Arduino



## History of the Arduino

---

In 2003 Hernando Barragan started working on a project called **Wiring** for his master's thesis at the **Interaction Design Institute Ivrea (IDII)** in Italy. At that time students used a microcontroller board that cost USD $100 and needed additional hardware and software to use. Massimo Banzi and Casey Reas, who is known for work on the Processing language, were supervisors for his thesis. The name was *Wiring: Prototyping Physical Interaction Design*.

>**You can view the thesis here**: http://people.interactionivrea.org/h.barragan/thesis/thesis_low_res.pdf.

The purpose of the thesis was to create a low-cost and easy-to-use tool so non-engineers could create digital projects. To do this, Hernando wanted to abstract away the complicated details of the electronics to let the user focus on their project. This meant that it had to be work by simply plugging the device into a host computer and have an easy-to-use interface to program it.

1. The first prototype used the **Parallax Javelin Stamp** microcontroller, which used a subset of the Java programming language. This solution required the Parallax proprietary tools to compile, link and upload the projects to the microcontroller; therefore, it did not meet the requirements of the project because the wiring was going to be an open source project.

1. The second prototype used the Atmel ARM-based **91R40008 microcontroller**. Hernando obtained better results with this new microcontroller; however, he determined that the microcontroller was far too complex, and it was almost impossible to solder it by hand to a circuit board.

1. The third prototype used the **Atmel ATmega128** microcontroller with the **MAVRIC** microcontroller board. Hernando had great success using this microcontroller. He used a tool written by Brian Dan called **Avrdude** to easily upload new programs to the board.


in 2005, the first Arduino board was created. The Arduino board used the less expensive ATmega128 microcontroller to reduce cost. The Arduino team forked the Wiring code and added support for this board.

The initial Arduino core team consisted of Massimo Banzi, David Cuartielles, Tom Igoe, Gianluca Martino and David Mellis. Hernando was not invited to participate in this project. There are several accounts from different individuals involved about why he was not invited.

The Arduino team strongly believed in open source hardware and software. They believed that by opening the platform up, many more people would have access to and be involved with it. Another reason for opening the platform up was that IDII had used up its funding and was going to be shut down. By open sourcing the platform they knew it would survive and would not be exploited by others.

The team initially decided on a price of USD $30 for the board. They figured it would make it easily accessible to students as well individuals. They also decided to make the board blue, which was different from most other boards at the time, which were green. Another design decision that helped add to the popularity of the board was giving it lots of input and output pins. Most boards at the time limited the number of I/O to reduce costs.

after a test, people began to hear about this board and wanted one for themselves. The project started to take off; however, it was still missing a name. While discussing the name, the team was having drinks at a local a bar frequented by Massimo Banzi. The bar's name was Bar Di Re Arduino and the new board became known as the Arduino.

### What is the Arduino?

At the heart of the Arduino is the microcontroller. A microcontroller is a standalone, singlechip integrated circuit that contains a CPU, read-only memory, random access memory and various I/O busses. Most Arduino boards use the Atmel 8-bit AVR microcontroller.

The Arduino UNO R3, uses the ATmega328 chip. This chip is an 8-bit RISC-based microcontroller that features 32 KB of flash memory with read-write capabilities, 1 Kbyte EEPROM, 2 Kbytes SRAM, 23-general purpose I/O lines and 32 general-purpose registers.

All the hardware and software that make up the Arduino platform are distributed as open source and licensed under the GNU Lesser General Public License (LGPL) or the GNU General Public License (GPL). This allows for the manufacture and distribution of Arduino boards by anyone and has led to numerous generic, lower cost, Arduino compatible boards.

> You can find more information about the license and the Arduino boards on the Arduino website here: https://www.arduino.cc.

>

## Touring the Arduino UNO R3

---

The Arduino is an open source hardware and software platform that is incredibly powerful yet easy to use. You can look at and download the code from any of the Arduino repositories on GitHub here: https://github.com/arduino. This platform has captured the imagination of electronic enthusiasts and the maker community everywhere. It enables people to inexpensively experiment with electronic prototypes and see their projects come to life. These projects can range from simply making an LED blink or recording the temperature to controlling 3D printers or making robots.

![](https://static.packt-cdn.com/products/9781788830584/graphics/assets/7c3fc9a6-b4f2-44b9-a745-5e8ead0f93f6.png)

As we can see, the Arduino Uno of today still uses the blue color that the original Arduino designers chose to help their boards stand out. The following is a list of major components of the Arduino Uno:

- DC supply Input: The DC supply input can be used with an AC-to-DC power adapter or a battery. The power source can be connected using a 2.1 mm centerpositive plug. The Arduino Uno operates at 5 volts but can have a maximuminput of 20 volts; however, it is recommended to not use more than 12V.
- Voltage Regulator: The Arduino uses a linear regulator to control the voltage going into the board
- USB Port: The USB port can be used to power and program the board.
- RESET button: This button, when pressed, will reset the board.
- ICSP for USB: The in-circuit serial programming pins are used to flash the firmware on the USB interface chip.
- ICSP for ATmega328: The in-circuit serial programming pins are used to flash the firmware on the ATmega microcontroller.
- Di-gital and PWM connectors: These pins, labeled 0 to 13, can be used as either a digital input or output pins. The pins labeled with the tilde (~) can also be used for Pulse-Width Modulation (PWM) output.
- Analog In Connectors: The pins, labeled A0 to A5, can be used for analog input. These pins can be used to read the output from analog sensors.
- Power and External Reset: These pins in this header, provide ground and power for external devices and sensors from the Arduino. The Arduino can also be powered through these pins. There is also a reset pin that can be used to reset the Arduino.
- ATmega328: The microcontroller for the Arduino Uno board.



## Powering the Arduino

---


The Arduino can be powered in one of three ways: through the VIN/GND pins, the DC Supply Input port or the USB port.

### Using the VIN/GND pins to power the Arduino (OPTION)

The VIN and GND pins in the power and external reset header can be used to power the Arduino with an external battery. Powering the Arduino in this way is mainly used when we wish to connect a battery, in series, with a switch to turn the power to the Arduino on and off. The following photograph illustrates this:

![](https://static.packt-cdn.com/products/9781788830584/graphics/assets/67e06754-5195-480b-bc27-476bdfeaba2f.png)

It is not recommended that we power the Arduino in this manner unless we are looking for the most expensive and short-lived way to power the Arduino. We could use six AA batteries in series, which will provide the same voltage as the 9V battery in the preceding photograph but would give us approximately four times the capacity. It is still not recommended that we power the Arduino in this manner as it would be fairly expensive. Unless there is a specific need to use a battery to power the Arduino, I would avoid using them.

### Using the DC supply input to power the Arduino

The DC supply input connector can be used with an AC-to-DC power adapter or a battery to power the Arduino. The connector has a female 2.1 mm center-positive plug. While the Arduino operates at 5 volts a maximum input of 20 volts can be used; however, as was stated earlier, it is recommended to not use more than 12V.We can use an AC-to-DC adjustable power adapter like the one shown in the following photograph to power the Arduino using the DC supply input connector:

![](https://static.packt-cdn.com/products/9781788830584/graphics/assets/974d7f0c-4f37-4022-ad01-d4b71072adcf.png)

With this adapter, you can adjust the output power to the desired voltage. You can find power supplies similar to this online or at most stores that sell electronic items.

###  Using the USB connector to power the Arduino

Using the USB connector to power the Arduino is the way that I usually power it. It is by far the easiest and safest way to power the Arduino and the least expensive. You can power the Arduino directly from the USB port on your computer or from a USB rechargeable power bank like the one shown in the following photograph:

![](https://static.packt-cdn.com/products/9781788830584/graphics/assets/77319c69-7b85-4599-927e-a67ec13a3631.png)


## Arduino shields

---

An Arduino shield is a modular circuit board that plugs directly into the pin headers of the Arduino board. These shields will add extra functionality to the Arduino board. If we are looking to connect to the internet, do speech recognition, control DC motors or add other functionality to the Arduino, there is probably a shield that can help us. While we are not required to use shields, they do make adding extra functionality to our Arduino boards very easy.

The following photograph shows examples of a few shields. We will be using shields in some of our sample projects later in this book:

![](https://static.packt-cdn.com/products/9781788830584/graphics/assets/c23d2894-1548-4ec0-bac9-5f8d37512bb9.png)


A shield fits on top of the Arduino by plugging directly into the pin headers. We can also stack one shield on top of another if they do not use the same resources. Here is how an Arduino looks with two shields attached:

![](https://static.packt-cdn.com/products/9781788830584/graphics/assets/f5c71be2-647a-4392-96d9-8ea7e8da6365.png)

An Arduino shield makes it incredibly easy to add functionality to an Arduino Uno. Most shields usually have great documentation as well, which makes programming them also very easy. The drawback to shields is they usually cost more than purchasing the components and connecting them to the Arduino with a breadboard. Some shields, such as the MOVI speech synthesizing and voice recognition shield and the Sparkfun Xbee radio module shield, add functionality that cannot simply be added as a single component. For functionality like this, a shield or an external circuit board would be required. Let's take a closer look at the pin headers for the Arduino Uno R3.





## Arduino pin

---

There is a total of 31 pins in the Arduino Uno pin headers.
Most of these pins can be configured to perform different functions. 

![](https://static.packt-cdn.com/products/9781788830584/graphics/assets/e02fd8cb-b102-48c1-94ea-dfb1810a644b.png)

### Digital pins
The digital pins on the Arduino are the ones that are used the most when connecting external sensors. These pins can be configured for either input or output. 

### Analog input pins
The analog input pins are used to read analog sensors such as rangefinders and temperature sensors. The six analog pins can also be configured as digital pins if we run out of digital pins in our project.

### PWM pins
Where the analog input pins are designed to read analog sensors (input), the PWM pins are designed for output. PWM is a technique for obtaining analog results with digital output.
We have the ability to set the frequency of how fast the signal can switch between HIGH and LOW. This frequency is measured in Hertz and sets how many times the signal can switch per second.

### Power pins

- VIN: This pin is used when we power the Arduino board using an external power supply. This is the pin used in the Using the VIN/GND pins to power the Arduino section of this chapter.
- GND: These are the ground pins.
- 5V: This is 5V out and is used to power most sensors.
- 3.3V: This is 3.3V out and can be used to power sensors that are compatible with 3.3V.
- Reset: This pin can be used to reset the Arduino board by an external source.
- ioref: This is the reference voltage for the board. For the Arduino, this will be 5V.

### Serial pins
These pins can be used for serial communication. 
These pins are connected directly to the USB-to-TTL serial chip.

### SPI pins
- MISO: The Master in Slave out pin is used to send data from the slave to the master device.
- MOSI: The Master out Slave in the pin is used to send data from the master to the slave device.
- SCK: The serial clock synchronizes the data transmission and is generated by the master.
- SS: The slave select pin tells the slave to go active or to go to sleep. This is used to select which slave device should receive the transmission from the master.





## Different Arduino boards

---

The most popular Arduino board is Arduino Uno R3, but there are a lot of different arduino boardsand modules that can be use for variuous purposes.

If you want to know all these arduino boards, you can go to that arduino product page (https://www.arduino.cc/en/Main/Products).

For this case, we are going to see a list from some of the popular boards:

### Arduino Micro:
This Arduino board is the smallest in the Arduino family. His microcontroller is a ATmega32U4.
![](https://cdn.shopify.com/s/files/1/0438/4735/2471/products/A000053_03.front._618x464.jpg?v=1626444584)
The board count with a total of 20 digital pins, 7 of these can be used for PWM output, and other 12 can be used as analog input.

### Arduino Mega 2560.
This board is designed for the mos complex projects for example pototipes or 3D printers.
It counts with a total of 53 digial I/O pins, 16 analog input pins and 15 PWM output pins. Aditional, it has 4 serial UARTs for serial connections.
![](https://www.electrontools.com/Home/WP/wp-content/uploads/2016/04/Arduino-mega.jpg)
### Lilypad.
This Arduino board is designet for wearable projects is designed for wearable projects. It can be sewn into fabrics and use power supplies and sensors that are also sewn into fabrics. The Lilypad is based on the ATmega168V or ATmega328V (low power versions). This board features 16 digital I/O, 6 analog inputs and 6 PWM outputs.
![](https://docs.arduino.cc/static/1a057094ced72ec250b014e92a58af22/a207c/lilypad_main.jpg)
### Arduino Nano.
This board has a lot of similarities with the Arduino Micro, but this was released before that Micro, Arduino Nano was released in 2008 and Micro in 2012.
This board has 14 digital I/O pins, 8 analog input pisn and 6 PWM output pins.
The Arduino Nano is easier to obtain than the Micro because there are so many generic Nano boards, and the majority of times, the Nano board is half price of the micro.
![](https://cdn.shopify.com/s/files/1/0438/4735/2471/products/A000005_04.back_618x464.jpg?v=1628695103)
### Generic boards
There is a lot of generic boards because Arduino is an open source hardware and software plataform.
An advantage of this boards is that they are cheaper and usually easier to obtain than the genuine Arduino boards.
In the next images we'll see some examples for generic boards like Arduino Uno and MEGA 2560.

![Generic Arduino Uno](https://http2.mlstatic.com/S_982625-MLM25478726468_042017-O.jpg)
![Generic Arduino Uno](https://cdn.shopify.com/s/files/1/0076/2098/4932/products/HTB1ljAUcLc3T1VjSZLeq6zZsVXao_1024x1024@2x.png?v=1563299512)


The first thing that we see is that these boards don't conrain the Arduino logo, but they still contain the name of the official board.
Some of the generic boards doesn't see like the genuine, some of manufactrers chose to take the Arduino reference design and add additional functionality to their boards. Example:

![](https://th.bing.com/th/id/OIP.nu7E8cAWe0j7YMlHoghSggHaHa?pid=ImgDet&rs=1)

The DFRobot RoMeo BLE board is an Arduino-compatible robot control board with Bluetooth LE 4.0. This board takes the design of the Arduino Uno and adds a number of extra features, such as built-in Bluetooth and an integrated two-way DC motor driver.








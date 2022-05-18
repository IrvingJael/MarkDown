# Chapter 1 
## The Arduino

---

### History of the Arduino
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

-DC supply Input: The DC supply input can be used with an AC-to-DC power adapter or a battery. The power source can be connected using a 2.1 mm centerpositive plug. The Arduino Uno operates at 5 volts but can have a maximuminput of 20 volts; however, it is recommended to not use more than 12V.
- Voltage Regulator: The Arduino uses a linear regulator to control the voltage going into the board
- USB Port: The USB port can be used to power and program the board.
- RESET button: This button, when pressed, will reset the board.
- ICSP for USB: The in-circuit serial programming pins are used to flash the firmware on the USB interface chip.
- ICSP for ATmega328: The in-circuit serial programming pins are used to flash the firmware on the ATmega microcontroller.
- Di-gital and PWM connectors: These pins, labeled 0 to 13, can be used as either a digital input or output pins. The pins labeled with the tilde (~) can also be used for Pulse-Width Modulation (PWM) output.
- Analog In Connectors: The pins, labeled A0 to A5, can be used for analog input.
- These pins can be used to read the output from analog sensors.
- Power and External Reset: These pins in this header, provide ground and power for external devices and sensors from the Arduino. The Arduino can also be powered through these pins. There is also a reset pin that can be used to reset the Arduino.
- ATmega328: The microcontroller for the Arduino Uno board.










# soldering-station
### ***based on Weller RT soldering tip***

History
----

 This soldering station is my own build version of the station shown in [Heise Make 05/2016](https://www.heise.de/select/make/2016/5/1476695937422186). I made this already in 2017 but never documented it. Now, during process of software update I thought it would be a good idea to document this project and make it available for the public. 
 Credits for original design goes to Luca Zimmermann.
 Original code is hosted here: [ArduinoHannover/Maiskolben](https://github.com/ArduinoHannover/Maiskolben). I have not forked the code from Luca in order to avoid doubling the information and wasting memory. 
 In order to make this customized build there is no need to have the original code. Nevertheless, you will find all informations regarding code history, features of the different versions as well as the user manual in the repository, which hosts the original code.
 
 I have created my own custom PCB, which is build into a standard housing from Hammond (type 1591C), so no need to make 3D Prints.
 The hardware is based on the original design. However the key layout has been adopted to my needs. The current software I'm using is release 2.8 with my modifications. The software can be found in an own repository:
 [soldering_station_software](https://github.com/Andy79881/soldering_station_software). Unfortunately I could not manage to add the repository as pure software repository within this one.

Below you find the changes to the original design from [ArduinoHannover/Maiskolben](https://github.com/ArduinoHannover/Maiskolben)

Baseline:
---
- code is based on release 2.8, which is the latest code supporting TFT displays based on ST7735. Note: V3.x is based on a different display library (ILI9163C).

Changes to original design and code:
----

- TFT backlight output added (Arduino pin D0). Backlight can be adjusted via potentiometer (no PWM controlled TFT brightness)
- modified definitions.h to cope with customized key layout and adding pin definition of TFT backlight discrete output (TFT_BL)
- customized PCB to fit into standard housing from Hammond (type 1591C)
- old fashioned ino file converted into cpp file format by following two steps (see [ino-to-cpp](https://docs.platformio.org/en/latest/faq/ino-to-cpp.html)).

Design decisions:
----
- Diptrace is used for schematics and PCB layout creation (note: free editition 4.x can be used)
- almost SMD components used (except 5V regulator, connectors, push buttons, LED and Arduino Nano)
- software environment changed to VSCode with PlatformIO (library dependencies added into platformio.ini)

Final Remarks:
---
- Code is provided **AS IS**, so no warranties.
- Code size is actually close to the limits. This may be also caused by using the latest library versions. Be aware of this if you make the build by yourself.

   

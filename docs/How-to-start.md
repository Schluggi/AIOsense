
# 1. PCB
First of all you need the PCB. We recommend PCBWay because its the most straight forward experience. Just click on the link and take your order (you can also use [this link³](https://pcbway.com/g/DFb536) for register to get 5$ off on your first order). But you can actually choose any PCB manufacturer.
Please notice that not all of them have the same capabilities. We tried to make our PCB as generic as possible, it should work for most of them but try this at your own risk. Below you can find a list of tested manufacturer.

- [PCBWay³](https://www.pcbway.com/project/shareproject/AIOsense_All_In_One_Sensor_132c1507.html) 
- [Aisler](https://aisler.net/p/TWDRHBSM) 

For all other manufacturer (like [JLCPCB](https://jlcpcb.com/)) please upload the zip file which you can find at the [release](https://github.com/Schluggi/AIOsense/releases/latest) page.



## More?
### I²C
We designed the Board with two generic I²C sockets. So feel free to use it for any other I²C based sensor. Just make sure the pinout is correct. Please let us know what works and what does not.

Your board in full of sensors, and you need more I²C pins? You can use the external IO pins (SDA & SCL).
<br><img src="https://user-images.githubusercontent.com/43608073/204273668-cbcb2d05-0535-4dfb-8d97-8d3b0530deb8.jpg" width="200" />


### SPI
> **Note**: Please read [this note](https://github.com/Schluggi/AIOsense/wiki/How-to-start-%3F#microphone-does-not-work-for-now)!

SPI is not used by the board, so you can use it via the external IO pins (MISO, MOSI, SCK, CS):
<br><img src="https://user-images.githubusercontent.com/43608073/204273762-27b1be06-36c0-450d-b37c-bb5408cde0f4.jpg" width="200" />


### Serial
Unfortunately there is only one serial connection possible which is used for the mmWave sensor. You can use these pins for serial if you don't want to use a mmWave sensor.


***

³ Affiliate link


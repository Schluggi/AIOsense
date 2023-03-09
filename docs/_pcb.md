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

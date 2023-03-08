> This is only related to v2.0

# 1. PCB
First of all you need the PCB. We recommend PCBWay because its the most straight forward experience. Just click on the link and take your order (you can also use [this link³](https://pcbway.com/g/DFb536) for register to get 5$ off on your first order). But you can actually choose any PCB manufacturer.
Please notice that not all of them have the same capabilities. We tried to make our PCB as generic as possible, it should work for most of them but try this at your own risk. Below you can find a list of tested manufacturer.

- [PCBWay³](https://www.pcbway.com/project/shareproject/AIOsense_All_In_One_Sensor_132c1507.html) 
- [Aisler](https://aisler.net/p/TWDRHBSM) 

For all other manufacturer (like [JLCPCB](https://jlcpcb.com/)) please upload the zip file which you can find at the [release](https://github.com/Schluggi/AIOsense/releases/latest) page.

# 2. CPU
You can use any ESP32 mini or ESP8266 mini with the correct pinout but we highly recommend the ESP32-C3.

|                 | ESP32-C3 (recommended)                                                                  | ESP32                                                                                                | ESP32-S2                                                                                | ESP8266                                                                                              |
|-----------------|-----------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| USB-Type        | Type-C                                                                                  | micro-USB                                                                                            | Type-C                                                                                  | micro-USB or Type-C                                                                                  |
| Bluetooth       | &check;                                                                                 | &check;                                                                                              | &check;                                                                                 | &cross;                                                                                              |
| Bluetooth LE    | &check;                                                                                 | &check;                                                                                              | ?                                                                                       | &cross;                                                                                              |
| Case            | &check;                                                                                 | &cross;(not yet)                                                                                     | &check;                                                                                 | &check;                                                                                              |
| external power¹ | &check;                                                                                 | &check;                                                                                              | &check;                                                                                 | &cross;                                                                                              |
| LED             | WS2812B RGB                                                                             | White                                                                                                | White                                                                                   | White                                                                                                |
| fits perfectly  | &check;                                                                                 | [stands over](https://github.com/Schluggi/AIOsense/issues/15#issuecomment-1399424459)                | &check;                                                                                 | &check;¹                                                                                             |
| Where to buy?   | [AliExpress](https://de.aliexpress.com/item/1005004740051202.html?gatewayAdapt=glo2deu) | [Amazon DE³](https://amzn.to/3UfjWid), [AliExpress](https://de.aliexpress.com/item/32858054775.html) | [AliExpress](https://de.aliexpress.com/item/1005003145192016.html?gatewayAdapt=glo2deu) | [Amazon DE³](https://amzn.to/3FWUFoO), [AliExpress](https://de.aliexpress.com/item/32529101036.html) |

¹ External power via the terminal connectors are not possible if the USB-connector is at the bottom (ESP8266).




# 3. Sensor Modules
Everything is completely modular and swappable. You can decide yourself which sensor you need and want to have.

## 🚶Motion Sensor (PIR)
You want a classic motion sensor? No problem. We would recommend an industrial standard EKMC1603111 ([Datasheet](https://www3.panasonic.biz/ac/ae/search_num/index.jsp?c=detail&part_no=EKMC1603111)). Every other 3V PIR sensor with an TO-5 3-pin socket should work as well (untested).
Please notice that you will need an TO-5 3-pin socket as well (in any case)!

Sensor:
- [Voelkner](https://www.voelkner.de/products/994091/Panasonic-PIR-Bewegungssensor-EKMC1603111-3-6V-1St..html)
- [Mouser](https://www.mouser.de/ProductDetail/Panasonic-Industrial-Devices/EKMC1603111?qs=7jYh1P364wm%252bee2n5xwlWg%3D%3D)
- [Farnell](https://de.farnell.com/en-DE/panasonic-electric-works/ekmc1603111/sensor-motion-12m-white/dp/2095731?st=ekmc1603111)
- [Digi-Key](https://www.digikey.de/de/products/detail/panasonic-electric-works/EKMC1603111/2601880)
- [RS-Online](https://de.rs-online.com/web/p/naherungssensoren-ics/1357081)

Socket: [Mouser](https://www.mouser.de/ProductDetail/Mill-Max/917-43-103-41-005000?qs=teNCaa%2FZ3auQVxVMs%2F5ihg%3D%3D)

## 🧍mmWave / Radar Sensor
Never heard before? It's a fancy technology to recognize smallest movements (like a motion sensor/PIR but really sensitive). This is useful in situations you want to track if someone is present even if the person is not really moving for example while watching TV or sleeping.

The board is mainly made for the SEN0395 [datasheet](https://wiki.dfrobot.com/mmWave_Radar_Human_Presence_Detection_SKU_SEN0395). There are two sockets for this sensor. Feel free to choose yourself which one do you prefer. It's just the orientation. There is no difference between these two and you can't use both sockets at the same time.

Shortly before release of V2.0 someone asked to support the much cheaper module HLK-LD2410 [datasheet](https://drive.google.com/drive/folders/1p4dhbEJA3YubyIjIIC7wwVsSo8x29Fq-?spm=a2g0o.detail.1000023.17.6dfa18b2xYoafU). So I added a socket. ~~There is no ESPHome code for this yet, so feel free to contribute your code.~~ This module is also supported in ESPHome now, see [here](https://esphome.io/components/sensor/ld2410.html).


SEN0395 (recommended):
- [Mouser](https://www.mouser.de/ProductDetail/DFRobot/SEN0395?qs=ljCeji4nMDmvEgq75EdCVA%3D%3D)
- [Farnell](https://de.farnell.com/en-DE/dfrobot/sen0395/mmwave-radar-board-arduino-board/dp/3879712)
- [Digi-Key](https://www.digikey.de/de/products/detail/dfrobot/SEN0395/14322660?s=N4IgTCBcDaIMoFEByAGAzATgKwgLoF8g)      

HLK-LD2410: [AliExpress](https://de.aliexpress.com/item/1005004351593073.html?spm=a2g0o.productlist.main.1.7d99569bRHd5zt&algo_pvid=26f5f6c1-cfdd-4c3c-b186-566c2cfb3ed3&algo_exp_id=26f5f6c1-cfdd-4c3c-b186-566c2cfb3ed3-0&pdp_ext_f=%7B%22sku_id%22%3A%2212000028862626467%22%7D&pdp_npi=2%40dis%21EUR%214.18%213.97%21%21%211.91%21%21%400b0a558a16695823917665301d0702%2112000028862626467%21sea&curPageLogUid=bucRiwoGGyws)

## 💡Illuminance / Light Sensor
You want to turn the light on by motion but only when it's necessary? So you want to know, how bright it is? We recommend the really cheap BH1750 module. 

- [Amazon DE³](https://amzn.to/3FVbLmP)
- [AliExpress](https://de.aliexpress.com/wholesale?catId=0&initiative_id=SB_20221127121631&SearchText=BH1750&spm=a2g0o.productlist.1000002.0&dida=y)

## 🌡️Temperature, Humidity, Pressure & Air Quality
For these measurements we recommend the industrial sensors BME680/BME688 or the BME280 (cheaper but without air quality).

Please notice that you can either use the BME280 **or** the BME680 out of the box (there have the same I²C address).

If you can solder SMD components you can solder them directly onto the PCB. Please notice that you will need and solder these three more components: 2x 4K7 resistor (THT), 1x 100nF capacitor (also SMD). Also important to know: It's not recommended to solder the BME680 with hot air because this can damage the air quality sensor. Use a hotplate instead.

Related to [#7](https://github.com/Schluggi/AIOsense/issues/7) sometimes SMD soldering can be inaccessible or difficult. You can use a small BME-Module on one of the generic I²S sockets instead. 

BME280 (Temperature, Humidity, Pressure)
- Module
  - [Amazon DE³](https://amzn.to/3XPo7DV)
  - [AliExpress](https://de.aliexpress.com/wholesale?catId=0&initiative_id=SB_20221127130157&SearchText=BME280+&spm=a2g0o.home.1000002.0&dida=y)
- SMD
  - [Reichelt](https://www.reichelt.de/kombo-sensor-luftdruck-luftfeuchtigkeit-temp--bme-280-p159825.html)
  - [Mouser](https://www.mouser.de/ProductDetail/Bosch-Sensortec/BME280?qs=2OnyuXx6vpj2fK9HX7qb3g%3D%3D)
  - [Digi-Key](https://www.digikey.de/de/products/detail/bosch-sensortec/BME280/6136306)

BME680 (Temperature, Humidity, Pressure & Air Quality)
- Module
  - [Amazon DE³](https://amzn.to/3VrcK2E)
  - [AliExpress](https://de.aliexpress.com/wholesale?catId=0&initiative_id=SB_20221127130036&SearchText=BME680+&spm=a2g0o.home.1000002.0&dida=y)
- SMD
   - [Reichelt](https://www.reichelt.de/kombo-sensor-luftdruck-luftfeuchtigkeit-temp-gas-bme-680-p159835.html)
   - [Mouser](https://www.mouser.de/ProductDetail/Bosch-Sensortec/BME680?qs=v271MhAjFHjo0yA%2FC4OnDQ%3D%3D)
   - [Digi-Key](https://www.digikey.de/de/products/detail/bosch-sensortec/BME680/7401317)

## 🎙️Microphone (does not work for now)
> **Note**: The mic uses some SPI pins. If you want to use the mic you **can not** use any generic device connected to the these IO-header pins: CS, SCK, MISO as well as any SPI based sensor at all.

We designed the board while having the future in mind. So the idea to have a microphone in each room for a voice assistant would be awesome. Unfortunately, ESPHome does not support this yet ([ESPHome feature request](https://github.com/esphome/feature-requests/issues/1254)). This in mind we can't test this at all but Open Home (the company behind ESPHome and Home Assisant) just [release there plans](https://www.youtube.com/watch?v=D936T1Ze8-4) for 2023 and mention that there is hope this will be implemented in the upcoming year.

The board is designed to work only with INMP441-modules which are known for their high quality digital audio.
- [Amazon DE³](https://amzn.to/3u2kRY3)
- [AliExpress](https://de.aliexpress.com/wholesale?catId=0&initiative_id=SB_20221127114658&SearchText=inmp441&spm=a2g0o.tm800107193.1000002.0&dida=y)

## More?
### I²C
We designed the Board with two generic I²C sockets. So feel free to use it for any other I²C based sensor. Just make sure the pinout is correct. Please let us know what works and what does not.

Your board in full with sensors and you need more I²C pins? You can use the external IO pins (SDA & SCL).
<br><img src="https://user-images.githubusercontent.com/43608073/204273668-cbcb2d05-0535-4dfb-8d97-8d3b0530deb8.jpg" width="200" />


### SPI
> **Note**: Please read [this note](https://github.com/Schluggi/AIOsense/wiki/How-to-start-%3F#microphone-does-not-work-for-now)!

SPI is not used by the board so you can use it via the external IO pins (MISO, MOSI, SCK, CS):
<br><img src="https://user-images.githubusercontent.com/43608073/204273762-27b1be06-36c0-450d-b37c-bb5408cde0f4.jpg" width="200" />


### Serial
Unfortunately there is only one serial connection possible which is used for the mmWave sensor. You can use these pins for serial if you don't want to use a mmWave sensor.


***

³ Affiliate link


# 🌡️Temperature, Humidity, Pressure & Air Quality
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


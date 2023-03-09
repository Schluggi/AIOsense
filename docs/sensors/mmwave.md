# 🧍Presence (mmWave/radar)

Never heard before? It's a fancy technology to recognize the smallest movements (like a motion sensor/PIR but really
sensitive). This is useful in situations you want to track if someone is present even if the person is not really moving
for example while watching TV or sleeping.

The board is mainly made for the
SEN0395 [datasheet](https://wiki.dfrobot.com/mmWave_Radar_Human_Presence_Detection_SKU_SEN0395). There are two sockets
for this sensor. Feel free to choose yourself which one do you prefer. It's just the orientation. There is no difference
between these two, and you can't use both sockets at the same time.

Shortly before release of V2.0 someone asked to support the much cheaper module
HLK-LD2410 [datasheet](https://drive.google.com/drive/folders/1p4dhbEJA3YubyIjIIC7wwVsSo8x29Fq-?spm=a2g0o.detail.1000023.17.6dfa18b2xYoafU).
So I added a socket. ~~There is no ESPHome code for this yet, so feel free to contribute your code.~~ This module is
also supported in ESPHome now, see [here](https://esphome.io/components/sensor/ld2410.html).

SEN0395 (recommended):

- [Mouser](https://www.mouser.de/ProductDetail/DFRobot/SEN0395?qs=ljCeji4nMDmvEgq75EdCVA%3D%3D)
- [Farnell](https://de.farnell.com/en-DE/dfrobot/sen0395/mmwave-radar-board-arduino-board/dp/3879712)
- [Digi-Key](https://www.digikey.de/de/products/detail/dfrobot/SEN0395/14322660?s=N4IgTCBcDaIMoFEByAGAzATgKwgLoF8g)

HLK-LD2410: [AliExpress](https://de.aliexpress.com/item/1005004351593073.html?spm=a2g0o.productlist.main.1.7d99569bRHd5zt&algo_pvid=26f5f6c1-cfdd-4c3c-b186-566c2cfb3ed3&algo_exp_id=26f5f6c1-cfdd-4c3c-b186-566c2cfb3ed3-0&pdp_ext_f=%7B%22sku_id%22%3A%2212000028862626467%22%7D&pdp_npi=2%40dis%21EUR%214.18%213.97%21%21%211.91%21%21%400b0a558a16695823917665301d0702%2112000028862626467%21sea&curPageLogUid=bucRiwoGGyws)

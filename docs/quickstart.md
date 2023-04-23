# Quickstart

## Order PCB

[![pcbway.png](img/pcbway.png)](https://www.pcbway.com/project/shareproject/AIOsense_All_In_One_Sensor_132c1507.html)

First of all you need the PCB. We recommend PCBWay because it's the most
straight forward experience and the quality is excellent. Just click on the link
and take your order (you can also use [this link³](https://pcbway.com/g/DFb536)
for register to get 5$ off on your first order). But you can actually choose any
PCB manufacturer. Please notice that not all of them have the same capabilities.
We tried to make our PCB as generic as possible, it should work for most of them
but try this at your own risk.

- [PCBWay³](https://www.pcbway.com/project/shareproject/AIOsense_All_In_One_Sensor_132c1507.html)
- [Aisler](https://aisler.net/p/TWDRHBSM)

For all other manufacturer (like [JLCPCB](https://jlcpcb.com/)) please upload
the zip file which you can find at
the [release](https://github.com/Schluggi/AIOsense/releases/latest) page.

## Order parts

Now that you have the PCB, we still need the remaining parts. There is a
separate [BOM (Bill Of Materials)](https://github.com/Schluggi/AIOsense/tree/main/bom)
for
each AIOsense version. Open the pdf file and order all green marked lines.

You can get most parts from sellers
like [Mouser](https://www2.mouser.com/), [Farnell](https://www.farnell.com/)
or [Digi-Key](https://www.digikey.com/). Direct links to the sensors can be
found [here](sensors.md).

Please make sure you pick the right BME680 module. It should look like
this: ![bme680-pcb](img/quickstart_bme680-pcb.jpg){: style="height:50%;width:
50%"}

More info about the BOM and what the groups are all about can be
found [here](bom.md).

## Assembly (wip)

Should be easy and self explainable.

## Flash ESPHome

[Click here](flashing.md).

## Further steps (optional)

- [Integrate Home Assistant](homeassistant.md).
- Print a case (wip)

<hr>
³ Affiliate link

My PCB prototypes are sponsored by PCBWay.
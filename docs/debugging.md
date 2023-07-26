# Debugging

## Inconsistent I²C readings

### I²C frequency

A first quick fix could be to choose a lower I²C frequency. In some cases this
can already help to improve consistently
readings. You can do this by tweaking your yaml file and add a `frequency`.

```yaml
i2c:
  frequency: 10kHz  # (defaults to 50kHz)
```

### Too many pull-up resistors ([#44](https://github.com/Schluggi/AIOsense/issues/44))

We need I²C pull-up resistors to make I²C to work. But since every module has
their own pull-ups, we're ending up with
too many pull-ups which can resolve in bad readings. This normally only happens
if you had soldered the two 4K7 Ohm
resistors and using the BME-Module (not the SMD version) as well as the
Light-Module.

The fix is easy: Remove both 4K7 Ohm resistors from the PCB.

![resistors.png.png](img/resistors.png)

## LD2410(c) does not work

Some versions of LD2410 and LD2410C behave somewhat peculiarly. If your ESP
cannot establish a connection to the mmWave module, it may help to swap the RX
and TX pins contrary to their labeling. To do this, simply adjust your ESPHome
config accordingly.

```yaml
# In this example, the pins are already swapped.
substitutions:

  # ESP32-C3 mini
  uart_rx_pin: GPIO21
  uart_tx_pin: GPIO20

  # ESP32-D1 mini
  uart_rx_pin: GPIO1
  uart_tx_pin: GPIO3

  # ESP32-S2 mini
  uart_rx_pin: GPIO39
  uart_tx_pin: GPIO37

  # ESP2866-D1 mini
  uart_rx_pin: GPIO1
  uart_tx_pin: GPIO3
```

Source: https://github.com/esphome/issues/issues/4317#issuecomment-1474937332
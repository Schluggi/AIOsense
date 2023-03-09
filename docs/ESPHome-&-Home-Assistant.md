# ESPHome Dashboard
First of all you need an ESPHome Dashboard. 

If you're using Home Assisant you can install it as an add-on by following [these instructions](https://esphome.io/guides/getting_started_hassio.html).
Otherwise, you can also install the dashboard [via pip](https://esphome.io/guides/installing_esphome.html) or by using the [docker container](https://esphome.io/guides/getting_started_command_line.html#installation).

# Config
Dashboard up and running? Great! Now you have to pick the ESPHome config for your chosen ESP/CPU. You can find a list of all available configurations [here](https://github.com/Schluggi/AIOsense/tree/main/esphome). 

Please make sure to replace `<secret>`-sections with real random secrets. Then follow the instructions on the dashboard to flash your ESP.

# Home Assistant
After AIOsense is up and running you can integrate your devices in Home Assisant by using [this integration](https://www.home-assistant.io/integrations/esphome/).

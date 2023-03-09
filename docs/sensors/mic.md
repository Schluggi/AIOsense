# 🎙️Microphone

> **Note**: The mic uses some SPI pins. If you want to use the mic you **can not** use any generic device connected to
> the these IO-header pins: CS, SCK, MISO as well as any SPI based sensor at all.

We designed the board while having the future in mind. So the idea to have a microphone in each room for a voice
assistant would be awesome. Unfortunately, ESPHome does not support this
yet ([ESPHome feature request](https://github.com/esphome/feature-requests/issues/1254)). This in mind we can't test
this at all but Open Home (the company behind ESPHome and Home Assisant)
just [release there plans](https://www.youtube.com/watch?v=D936T1Ze8-4) for 2023 and mention that there is hope this
will be implemented in the upcoming year.

The board is designed to work only with INMP441-modules which are known for their high quality digital audio.

- [Amazon DE³](https://amzn.to/3u2kRY3)
- [AliExpress](https://de.aliexpress.com/wholesale?catId=0&initiative_id=SB_20221127114658&SearchText=inmp441&spm=a2g0o.tm800107193.1000002.0&dida=y)

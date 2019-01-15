# OLED SSD1306 Library

You can choose from different ESPa nd OLED modules by entering the configuration:
```bash
make menuconfig
```
Then go to `Component config`, `OLED` and choose your board, if available.
If your board is not available, just select `other Board`, which will give you the possibility
to select the Pins and the size of the OLED Display manually.

## Fonts
| Num | Description | Size | Norm |
|-----|-------------|------|------|
|0 | bitocra |4x7 |ascii|
|1 | bitocra |6x11 |iso8859 1|
|2 | bitocra |7x13 |iso8859 1|
|3 | glcd |5x7|
|4 | roboto |8pt|
|5 | roboto |10pt|
|6 | terminus |6x12 |iso8859 1|
|7 | terminus |8x14 |iso8859 1|
|8 | terminus |10x18 |iso8859 1|
|9 | terminus |11x22 |iso8859 1|
|10 | terminus |12x24 |iso8859 1|
|11 | terminus |14x28 |iso8859 1|
|12 | terminus |16x32 |iso8859 1|
|13 | terminus bold |8x14 |iso8859 1|
|14 | terminus bold |10x18 |iso8859 1|
|15 | terminus bold |11x22 |iso8859 1|
|16 | terminus bold |12x24 |iso8859 1|
|17 | terminus bold |14x28 |iso8859 1|
|18 | terminus bold |16x32 |iso8859 1|



## ESP32 I2C OLED SSD1306 library for esp-idf
This is a library of i2c oled ssd1306 for [esp-idf](https://github.com/espressif/esp-idf).
Code modified from [ESP-I2C-OLED](https://github.com/baoshi/ESP-I2C-OLED).
I changed the hardware i2c driver into a software one. So you can use any two GPIO pins as SDA and SCL.
Remember to call **ssd1306_refresh** after you draw something new on the screen.
External RESET pin function is not implemented yet.
Although this lib supports two devices connecting to one i2c bus, I strongly recommend that you connect only one device to one i2c bus at the same time because I haven't tested it. I believe that the gpio pins on esp32 is enough for you to use.


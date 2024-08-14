# ESP32 (+S3, P4) AMY dual core example

An ESP-IDF implementation of running [AMY](https://github.com/shorepine/AMY) in dual cores.

## How to use example

Set your I2S pins at the top of `hello_world_main.c`:

```c
#define CONFIG_I2S_BCLK 25
#define CONFIG_I2S_LRCLK 36
#define CONFIG_I2S_DIN 32
```

Install and export the [ESP-IDF](https://github.com/espressif/esp-idf). For the P4, use the `master` branch.

Compile and flash your board, setting the `IDF_TARGET` to whatever you're using 
```bash
idf.py -DIDF_TARGET=esp32p4 flash
```

You should hear up to 20 polyphonic Juno-6 voices play out your I2S speaker. This uses both cores.





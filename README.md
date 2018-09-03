# M24SR Driver

This is a driver needed by `NFCEPROOM` constructor for the ST M24SR NFC chip.

## Requirements

This driver requires the ST M24SR NFC chip. This is present on the DISCO_L475VG_IOT01A and the X_NUCLEO_NFC01A1 shield.

## Configuration

Driver needs to be instantiated with valid pin names for I2C communication, GPO and RF disable pin. On a DISCO_L475VG_IOT01A these are configured by default.

If you are using a X_NUCLEO_NFC01A1 shield please edit `mbed_lib.json` and set the value of `X_NUCLEO_NFC01A1` to `true`. This will set appropriate defaults for you.

Otherwise, the driver will require passing valid pin names during instantiation explicitly.

## Building instructions

Driver will be built as part of the mbed-os build. Place the driver in the root directory of the mbed-os application. This can be done by placing a `.lib` file in the root of your application with a repository address with the driver. For example, to include this driver you can create a file called `eeprom_driver.lib` with these contents:

```
https://github.com/ARMmbed/mbed-nfc-m24sr
```

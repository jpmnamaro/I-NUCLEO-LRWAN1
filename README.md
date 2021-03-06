# I-NUCLEO-LRWAN1

Arduino library to support I-NUCLEO-LRWAN1 LoRa® expansion board based on USI®
LoRaWAN™ technology module.

## API

This library provides an Arduino API to manage the I-NUCLEO-LRWAN1 expansion
board as a LoRaWAN™ node.

* You will be able to choose the ABP or OTAA mode and set the corresponding keys.
* Send and receive some data.
* Select the EU or US band.
* Enable or disable the duty cycle (must be enabled in EU band).
* Enable the adaptative data rate and configure the data rate.
* Put the device in sleep mode.

This library provides also an API to manage the I-NUCLEO-LRWAN1 expansion board
as a simple LoRa® radio module.

* Configure the radio parameters (frequency, tx power, spreading factor, band width, ...)
* Send/receive data
* LoRaWAN stack disabled

## Known limitations

* The module supports only class A.
* Sleep mode is not supported in OTAA mode with the version 2.6 of the firmware.
* The same USART is shared between I-NUCLEO-LRWAN1 LoRa® expansion board and
Nucleo-64 boards. See UM1724, §6.8 section to solve the issue.

## Examples

* **getDevEUI**: display the unique device EUI.
* **LoRaWANABP**: send/receive data in ABP mode.
* **LoRaWANOTAA**: send/receive data in OTAA mode.
* **LoRaPingPong**: P2P exchange in LoRa®

## Advice

LoRaWAN default configuration:

* Join accept delay is set to 5000 ms (LoRaWAN default value).
* The network type is public by default. Use `setPublicNwkMode()` to set the network
type in private.
* RX1 window delay is 1000 ms by default. Use `setRx1Delay()` to set a new value.

In case of high latency between the gateway and the network server, it is recommended
to increase the delay time of the RX1 window.

## Version

This library is based on the STM32CubeExpansion_LRWAN_V1.1.2 driver.
This library has been validated with the version 2.6 of the firmware.

## Documentation

You can find the source files at  
https://github.com/stm32duino/I-NUCLEO-LRWAN1

The I-NUCLEO-LRWAN1 module datasheet is available at  
https://github.com/USILoRaModule/USI_I-NUCLEO-LRWAN1

LoRaWAN standard  
https://www.lora-alliance.org

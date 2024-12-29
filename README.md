# ESPhome_ButtonPlus

*ESPHome documentation and examples to make ESPHome working on the Button+*

## Button+

The Button+ is a modular control panel for home automation systems. It is designed to work with MQTT. It has several modules: a "Base module", a "Main display" and "BAR modules" where the position and amount can be changed according your needs. 

__You can order the Button+ on there [website](https://button.plus).__ this is also the place to find the original firmware, in case you want to revert back.

To make the Button+ work with ESPHome we needed at least a list of used components and a pinout/IO-list. I spend a couple of evenings with my multimeter, making my wife crazy with the beeps, googled and collected data sheets of the components, broke a the display of 1 BAR module and did a trail-on-error to make stuff work with ESPHome. Here in this repo you'll find the [results](./Components) of my journey. 
 
The ESPHome integration adds more flexibility and features, but also add some more complexity. To minimize the complexity I started this repo to collect examples and improve my work.

> Want to help? Pull requests are welcome!

[Dutch support topic on Tweakers.net](https://gathering.tweakers.net/forum/list_messages/2270086)
<!-- 
[English support topic on Home Assistant Community:](https://)
TODO
 -->
 
## Changes:

### NEXT: 0.2.0
#### NEW:
- added display item card (thanks @balk77)
- menu can now be controlled from HA and has page naming (thanks @balk77)

#### BREAKING:
- global `nr_of_pages` is now replaced by `nr_of_pages` ***substitution***, if you have compile errors please see the basic examples
- paging is now indexed by 1 > first page has number 1. Page 0>1, 1>2 etc.


### 0.1.1
Serialized the mini displays, by toggling the CS pins we need only 1 display instance now.

### 0.1.0
Created a Package

### Before 0.1.0
versions with first prove of concepts

## Documentation

The documentation of the Button+ ESPHome integration can be found in the [Docs directory](./Docs)

## Useful Links

* Display Items: https://esphome.io/components/display/
* Fonts: https://esphome.io/components/font#display-fonts
* Icon's and images: https://esphome.io/components/image#display-image

## Status

All the features the Button+ has to offer should work with the [`3pages_TotalExample.yaml`](./Examples/3pages_TotalExample.yml). Please refer the ESPHome documentation for more information on how to build your own menu or ... (?)

The documentation is work in progress.. Again If you want to help... Pull requests are welcome!

## TODO:

- [x] Neonleds
	- [x] figure out how to control them individually. [> maybe with Light Partition](https://esphome.io/components/light/partition)
	- [x] find correct [type](https://esphome.io/components/light/neopixelbus.html#configuration-variables)
- [x] Temperature sensor STS35
- [x] Make a basic [package](https://esphome.io/components/packages.html) so there is less initial code to be copied.
- [ ] Documentation
- [ ] More examples

# ESPhome_ButtonPlus

*ESPHome documentation and examples to make ESPHome working on the Button+*

<img src="./Docs/ButtonPlusImage.png" alt="Buttonplus running ESPhome" width="300" height="397"/>

## Button+

The Button+ is a modular control panel for home automation systems. It is designed to work with MQTT. It has several modules: a "Base module", a "Main display" and "BAR modules" where the position and amount can be changed according your needs. 

__You can order the Button+ on there [website](https://button.plus).__ this is also the place to find the original firmware, in case you want to revert back.

To make the Button+ work with ESPHome we needed at least a list of used components and a pinout/IO-list. I spend a couple of evenings with my multimeter, making my wife crazy with the beeps, googled and collected data sheets of the components, broke a the display of 1 BAR module and did a trail-on-error to make stuf work with ESPHome. Here in this repo you'll find the [results](./Components) of my journy. 
 
The ESPHome integration adds more flexebility and features, but also add some more complexity. To minimize the complexity I started this repo to collect examples and improve my work.

> Want to help? Pull requests are welcome!

[Dutch support topic on Tweakers.net](https://gathering.tweakers.net/forum/list_messages/2270086)
<!-- 
[English support topic on Home Assistant Community:](https://)
TODO
 -->
 
## Usefull Links

* Display Items: https://esphome.io/components/display/
* Fonts: https://esphome.io/components/font#display-fonts
* Icon's and images: https://esphome.io/components/image#display-image

## Documentation

The documentaion of the Button+ ESPHome integration can befound in the [Docs directory](./Docs)

## Status

All the features, i the Buton+ has to offer should work with the [`basic_example.yaml`](./Examples/basic_example.yaml). Please reffer the ESPHome documentaion for more information on how to build your own menu or ... (?)

The documentaion is yet to be made... Again If you want to help... Pull requests are welcome!

## TODO:

- [x] Neonleds
	- [x] figure out how to control them individually. [> maybe with Light Partition](https://esphome.io/components/light/partition)
	- [x] find correct [type](https://esphome.io/components/light/neopixelbus.html#configuration-variables)
- [x] Temperature sensor STS35
- [ ] Make a basic [package](https://esphome.io/components/packages.html) so there is less initial code to be copied.
- [ ] Documentation
- [ ] More examples

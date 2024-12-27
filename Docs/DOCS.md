# ESPHome Button+ Integration

*work in progress*

## Initial firmware load

### Required

- Button+ Base Module
- 1x Button+ Main Display
- 1x Button+ BAR module
- USB-C cable
- ESPHome installed on Home-Assistant  
    - [Getting started guide by @balk77](./GettingStarted.md)
    - [Official ESPhome guide](https://esphome.io/guides/getting_started_hassio.html)
- Chrome/Edge or a [WebSerial compatible Browser](https://webserial.io/)

### Steps

1. Go to ESPHome in Home Assistant.
2. Click on the bottom right on "Add Device"
3. Click "Continue"
4. Give the device a name you can remember (e.g. "Button+ Kitchen") and click "Next"
5. Click "Skip This Step"
6. Select the "ESP32-S3"
7. Click "Skip"
8. On the ESPHome main screen find the device you've just created, on the device card click "Edit"
9. Find in the links below the initial script for your setup. Copy
    - [1 BAR 1 Display](../Examples/1BAR_1Display_Basic.yaml)
    - [2 BAR 1 Display](../Examples/2BAR_1Display_Basic.yaml)
    - [3 BAR 1 Display](../Examples/3BAR_1Display_Basic.yaml)
10. Klik rechts boven in op "Save" en vervolgens op "Install"
11. Kies "Plug into this computer" en volg de instructies. Als je Firefox gebruikt kun je ook "Manual Download" kiezen en de image met ESP tool laden

Na de initiële upload met USB kun je de Button+ met de Wireless optie laden.

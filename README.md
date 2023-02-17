# RP2040-Zero ADXL345 Connection Klipper

## Connect your ADXL345 to your host Raspberry Pi via a RP2040-Zero

<img src="./images/rpi.jpg" width="300" alt='Raspberry Pi'/><img src="./images/RP2040-Zero.jpg" width="400" alt='RP2040-Zero'/><img src="./images/ADXL345.jpg" width="175" alt='ADXL345'/>

## My mounting solution for the Sovol SV06

I use this on my Sovol SV06. I *highly* recommend using short cables.

<img src="./images/setup1.jpg" width="400" alt='Setup 1'/> <img src="./images/setup2.jpg" width="400" alt='Setup 2'/> 

## Diagram
![Diagram](./images/diagram.png)

## Config

```
[mcu RP2040]
baud: 115200
restart_method: command
# Obtain definition by "ls -l /dev/serial/by-id/"
serial: /dev/serial/by-id/usb-Klipper_rp2040_E66138935F154C28-if00

[adxl345]
cs_pin: RP2040:gpio1
spi_bus: spi0a
```

## Sources

- [Link to the Sovol SV06 ADXL345 Mounting Solution](https://www.printables.com/model/385334-sovol-sv06-adxl345-mount-printhead-and-bed)
- [Link to my Sovol SV06 Klipper Config](https://github.com/bassamanator/Sovol-SV06-firmware/tree/master)

- https://github.com/Travis90x/TwoTrees-Sapphire-Plus-SP5-Marlin/tree/default/Klipper-Firmware
- https://travis90x.altervista.org/klipper-adxl345-raspberry-pi-rp2040-zero/?doing_wp_cron=1675003889.0499060153961181640625
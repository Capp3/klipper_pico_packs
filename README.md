# klipper_pico_packs

## Pico Packs for use with Klipper 3D printing firmware

This is a project to develop a secondary MCU for [Klipper3D](https://www.klipper3d.org/) using a [Raspberry Pi Pico](https://www.raspberrypi.com/products/raspberry-pi-pico/).

The genesis of this project is moving into Klipper with an older control board that wasnt built with all of the fancy interfacing that is avilable on purpose built Klipper boards. Or really just newer boards in general. My smoothie cone works well and I dont want to replace it just to add 

There are two flavours of packs here, a very tiny one meant to sit over top of a Pico with the same footprint. This has limited connectivity, but is quick and cheap, using connectors and bits I have laying about.

The "non-pico" is a larger pack meant to have the Pico sit on top of using the headers and can be bought pre-installed. This includes a larger assorment of connections and support components, notably some power regulation for driving Neopixels.

## Klipper problems with the RP2040

The RP2040 chip has had some documented problems related to reset with Klipper, I have implemented this solution;

### Workaround to connect rp2040 on startup or reboot

This is a *Work In Progess!!*

Install `uhubctl` a [utility for controlling USB power on the host microprocessor](https://github.com/mvp/uhubctl)

This may need to be adjusted for the specific USB port that the unit is connected to.

```bash
sudo apt install uhubctl
```

Next, edit `rc.local`

```bash
sudo nano /etc/rc.local
```

place this before `exit 0`

```bash
uhubctl -l 1-1 -a 2
sleep 1 && uhubctl -l 1-1 -a 2
```

## Pico Pack

Simple, simple, simple. This is mostly an exercise in develpment. This setup is mostly reflecting what I have put on a breadboard.

### Connections

SPI connections are seperated into "Data" and "Power" connectors. Both for space constrants. and because the assortment of JST connectors I have only go to 5 position!! Power connections include 2 GND positions to allow for grounding the shield of SPI, if present.

| Connector | Description         | Klipper Pins | Pico Pins |
| --------- | ------------------- | ------------ | --------- |
| J1        | VBUS(5v)/3.3v Power | NA           | NA        |
| J2        | VBUS(5v)/3.3v Power | NA           | NA        |
| J3        | SPI0                | spi0b        | SPI0/1    |
| J4        | SPI1                | spi1a        | SPI1/4    |
| J5        | IO0                 | gpio27       | 32        |
| J6        | IO1                 | gpio26       | 31        |
| J7        | I2C                 | i2c0f        | 20/21     |

The board design includes provisions for adding i2c pullup resistors to 3.3v. i2c interface only compatible at 3.3v for supply and signal.

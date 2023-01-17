# klipper_pico_packs

## Pico Packs for use with Klipper 3D printing firmware

This is a project to develop a secondary MCU for [Klipper3D](https://www.klipper3d.org/) using a [Raspberry Pi Pico](https://www.raspberrypi.com/products/raspberry-pi-pico/).

There are two flavours of packs here, a very tiny one meant to sit over top of a Pico with the same footprint. This has limited connectivity, but is quick and cheap, using connectors and bits I have laying about.

The "non-pico" is a larger pack meant to have the Pico sit on top of using the headers and can be bought pre-installed. This includes a larger assorment of connections and support components, notably some power regulation for driving Neopixels.

## Klipper problems with the RP2040

The RP2040 chip has had some documented problems related to reset with Klipper, I have implemented this solution;

### Workaround to connect rp2040 on startup or reboot

Install `uhubctl` a [utility for controlling USB power on the host microprocessor](https://github.com/mvp/uhubctl)

This may need to be adjusted for the specific USB port that the unit is connected to. I am still playing with this.

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

| Connector | Description |
| --------- | ----------- |
| J1
| J2

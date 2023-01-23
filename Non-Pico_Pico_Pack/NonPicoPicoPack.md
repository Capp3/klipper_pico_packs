# Non-Pico Pico Pack

The bigger version. My intention is to do this both as SMD and THC as an exercise. And THC would be a lot easier to do at home without special equipment.

## Connections and Pins

### Power Input

12-24v DC input, produces ~3amp for use with a MIC29500 fixed voltage reg.

| Pin | Desc            |
| --- | --------------- |
| 1   | 12-24 vdc Input |
| 2   | Ground          |

An extra connection is included for powering the Pi using the Onboard 5V labeled "PI_PWR"

| Pin | Desc  |
| --- | ----- |
| 1   | 5 vdc |
| 2   | Gnd   |

### BL Touch Connection

BL touch connection on a 5 pin JST

| Pin | Pico Pin | Description |
| --- | -------- | ----------- |
| 1   | gpio22   | Probe       |
| 2   | NA       | GND         |
| 3   | gpio28   | Servo       |
| 4   | NA       | 5V          |
| 5   | NA       | GND         |

### FAN Connections

Fan connection controlled by gpios. Voltage is sames as supply (12-24v)

#### FAN0

| Pin | Pico Pin | Desc |
| --- | -------- | ---- |
| 1   | NA       | VDC  |
| 2   | gpio18   | GND  |

#### FAN1

| Pin | Pico Pin | Desc |
| --- | -------- | ---- |
| 1   | NA       | VDC  |
| 2   | gpio19   | GND  |

### IO Ports

Two general IO ports with no supporting circuitry, be careful! Can be used as ins or outs, intention for replay control

#### IO0

| Pin | Pico Pin |
| --- | -------- |
| 1   | gpio26   |
| 2   | GND      |

#### IO1

| Pin | Pico Pin |
| --- | -------- |
| 1   | gpio27   |
| 2   | GND      |

### SPI Connections

A little odd here. Seperated the data and power to accomidate the assotment of connectors I have. Added an extra GND to the power connection to allow for sinking the shield per the klipper docs on cabling. Have 2 ports here

#### SPI Power Jumper

Set the voltage for the SPI power connections. Make sure you understand this and the unit you are connecting!!

| Pin | Desc |
| --- | ---- |
| 1   | 5vdc |
| 2   | Common Power |
| 3   | Pi 3.3vdc |

#### SPI Power Connections

| Pin | Desc |
| --- | ---- |
| 1   | GND  |
| 2   | PWR  |
| 3   | GND  |

#### SPI0

| Pin | Pico Pin | Desc |
| --- | -------- | ---- |
| 1   | gpio04   | MISO |
| 2   | gpio07   | MOSI |
| 3   | gpio06   | SCLK |
| 4   | gpio05   | CS   |

#### SPI1

| Pin | Pico Pin | Desc |
| --- | -------- | ---- |
| 1   | gpio08   | MISO |
| 2   | gpio11   | MOSI |
| 3   | gpio10   | SCLK |
| 4   | gpio09   | CS   |

### I2C

2 12c connections with selectable power

#### i2c Power Jumper

| Pin | Desc |
| --- | ---- |
| 1   | 5vdc |
| 2   | Common Power |
| 3   | Pi 3.3vdc |

#### i2c Connectors

Connections

| Pin | Pico Pin | Desc |
| --- | -------- | ---- |
| 1   | NA       | Pwr  |
| 2   | gpio21   | SDA  |
| 3   | gpio20   | SCL  |
| 4   | NA       | GND  |

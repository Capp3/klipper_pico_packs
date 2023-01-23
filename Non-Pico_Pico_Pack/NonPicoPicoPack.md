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

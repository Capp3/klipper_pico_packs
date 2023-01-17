# RPi Pico Hardware Reference information

## RPi Pico Hardware info

Information related to the Picos hardware and pin configs and how Klipper references them.

### Pico Pins

Find all Pico Pins here

[Pico Pinout Diagram](https://pico.pinout.xyz/)

### SPI Bus info

Two buses, but avilable on differnt pins. alias are as diffined in Klipper.

| Bus     | Alias | RX/MISO | TX/MOSI | SCK    | CS     |
| ------- | ----- | ------- | ------- | ------ | ------ |
| SPI0/0  | spi0a | gpio0   | gpio3   | gpio2  | gpio1  |
| SPI0/1  | spi0b | gpio4   | gpio7   | gpio6  | gpio5  |
| SPI0/2  | spi0c | gpio16  | gpio19  | gpio18 | gpio17 |
| SPI0/3* | spi0d | gpio20  | gpio23  | gpio22 |        |
| ------- | ----- | ------- | ------- | ------ | ------ |
| SPI1/4  | spi1a | gpio8   | gpio11  | gpio10 | gpio9  |
| SPI1/5  | spi1b | gpio12  | gpio15  | gpio14 | gpio13 |
| SPI1/6* | spi1c | gpio24  | gpio27  | gpio26 |        |

*- Pins are defined in the Klipper Code, but not marked on most Pico pinouts

### i2c Bus info

| Alias | SDA    | SCL    |
| ----- | -----  | ------ |
| i2c0a | gpio0  | gpio1  |
| i2c0b | gpio4  | gpio5  |
| i2c0c | gpio8  | gpio9  |
| i2c0d | gpio12 | gpio13 |
| i2c0e | gpio16 | gpio17 |
| i2c0f | gpio20 | gpio21 |
| i2c0g | gpio24 | gpio25 |
| i2c0h | gpio28 | gpio29 |
| i2c1a | gpio2  | gpio3  |
| i2c1b | gpio6  | gpio7  |
| i2c1c | gpio10 | gpio11 |
| i2c1d | gpio14 | gpio15 |
| i2c1e | gpio18 | gpio19 |
| i2c1f | gpio22 | gpio23 |
| i2c1g | gpio26 | gpio27 |

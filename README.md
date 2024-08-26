# ![Title Saying Hackboard](https://raw.githubusercontent.com/AdamTuraj/hackboard/main/Images/logo.png)

**Every hardware hacker needs a development board. So why not make your own overkill one?**

The Hackboard is a one board fits (almost) all development board with many useful features to ensure it works with all projects! Some of the features can be found below.

![A 3d view of the hackboard](https://raw.githubusercontent.com/AdamTuraj/hackboard/main/Images/3D_View.png)

Hackboard has the following features:

- 80MHz Cortex M4 Core with 1 Mb of Flash and 128 Kb of SRAM
- 45 GPIO pins
  - 2 SPI Interfaces[^1]
  - 1 I2C Interface
  - 1 CAN Interface
  - 1 UART Interface
  - 18 PWM Pins
  - 9 ADC's (Analog pins)
  - 2 DAC's
  - 1 OPAmp
- Arduino Uno Shield Compatible
- Same hole arrangement as Arduino UNO[^2]
- Extended header pads for easy probing
- Micro SD card slot
- PWM Addressable MOSFET capable of powering up to 54W
- 3 addressable LED's
- Barrel jack supporting up to 32V at 54W
- USB C port for flashing and power

[^1]: Only one may be used when an SD card is in use.
[^2]: The bottom right hole moved slightly up due to spacing issues.

## Assembly

> [!WARNING]
> This board CANNOT be assembled through JLCPCB due to many of the parts not being available at LCSC. Alternatives are using different PCB manufacturers or assembling it yourself

The BOM can be found in the production folder or the Digikey list [here](https://www.digikey.ca/en/mylists/list/BNXJM32ETT).

The extra MOSFET and related circuitry on pin 13 does not need to be soldered for the board to function (hence the DNP).

### Jumpers

JP1 and JP2 are jumpers that can be soldered/desoldered to achieve certain functionality.

JP1 must be bridged to enable the addressable LED's. JP2 must be left unbridged if the MOSFET is soldered.

### Work with Arduino

> [!NOTE]
> You must have an STLink to continue. They can be bought standalone or with a Nucleo board

A more detailed guide will be written up shortly. For now you may use [STM32Duino](https://github.com/stm32duino/Arduino_Core_STM32) to make it work with Arduino.

## License

Hackclub is licensed under the GNU General Public License. See the full license text in [LICENSE](LICENSE).

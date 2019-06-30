# Awesome PCB
This list contains awesome pcb-design related things.

## Content
- [ICs and Components](#components)
- [Part shops](#shops)
- [PCB Manufacturing](#manufacturing)
- [PCB Assembly](#assembly)
- [EDA Software](#software)
- [Design Guidelines](#guidelines)

## <a name="components"></a>ICs and Components
### <a name="components_voltage_regulators"></a>Voltage Regulators
- **LM317T** variable linear power supply, widely available
- **LM78xx** fixed voltage linear power supply, available in 3.3V, 5V and 12V (and many other voltages)
- **LM2596** Buck Converter, variable output voltage 1.23V - 37V, 3A max output, 40V max input
**LT1767** Monolithing 1.5A Step Down Regulator, 1.25 Mhz Switching frequency, Fixed output voltages of 1.8V, 2.5V, 3.3V and 5V, 2% output tolerance

### <a name="components_computing_storing"></a>Computing/Storage
- **‎W25Q series** SPI flash memory
- **‎STM32F103C8T6** Cheap microcontroller, same as on bluepills, 48 Mhz, ADC, I<sup>2</sup>C, SPI, USB
- **STM32F417** Bigger and faster alternative for the F103, F417/F427 have crypto hardware, F407 does not, 168 Mhz, ADC/DAC, I<sup>2</sup>C, SPI, USB, Ethernet
- **STM32F767** Bigger and even faster than the F417, Nucleo Board available
- **STM32G0 series** Next generation alternative for STM's _F0_ series.

### <a name="components_mosfet"></a>Mosfets & Switches
- **‎FQP30N06L** Beefy logic level mosfet V<sub>DSS</sub> 60V, I<sub>D</sub> 32A, R<sub>on</sub> 35mOhm, V<sub>gs<sub>th</sub></sub> < 2.5V, around 10A @ 3.3V V<sub>gs</sub>
- **BSS806NE** Super low threshold voltage, small package, V<sub>gs<sub>th</sub></sub> < 0.75V, V<sub>DS</sub> 20V, I<sub>D</sub> 2.3A
- **LTC2950** Pushbutton On/Off controller, adjustable turn on/off timers, debounced, µController interrupt & turn off pins, 2.7V - 26.4V
- **IS31FL3741** 39x9 dot matrix led driver, drives 351 leds or 117 rgb leds, I2C interface

### <a name="components_opamp"></a>Operational Amplifiers
- **LM358** Simple dual OpAmp, not great, not terrible

##  <a name="shops"></a>Part shops
- [Digikey](https://digikey.com) they have pretty much everything, US based
- [LCSC](https://lcsc.com) very cheap and good assortment of parts, from China

## <a name="manufacturing"></a>PCB Manufacturing
- [PCB Shopper](https://pcbshopper.com/) compares many pcb manufacturers
- [JLCPCB](https://jlcpcb.com/) 2$ for 10 PCBs
- [Elecrow](https://www.elecrow.com/services.html)
- [Seeed](https://www.seeedstudio.com/fusion.html)

## <a name="assembly"></a>PCB Assembly
- [PCB Shopper](https://pcbshopper.com/) compares many pcb assemblers
- [Elecrow](https://www.elecrow.com/services.html)
- [Seeed](https://www.seeedstudio.com/fusion.html)

## <a name="software"></a>EDA Software
- [KiCAD](http://kicad-pcb.org/) free and open source EDA software, had some pretty big updates and improvements recently
- [geda](http://pcb.geda-project.org/) free and open source
- [EAGLE](https://www.autodesk.de/products/eagle/free-download) free for smaller boards
- Altium Designer, not free or open source
- Orcad, not free or open source

## <a name="guidelines"></a>PCB Design guidelines/recommendations
Please note that the following guidelines/recommendations are not "official" in any way. They are merely the result of my own experience designing PCBs.
- Add test pads for power, ground and important signals
- Put pin names on the PCB
- Put reference designators for every component on the PCB
- Don't use text smaller than 1mm
- Add more test pads for ground (and other voltages/signals)
- Put polarity icon(s) on the silkscreen next to power connections
- Put min and max voltage on the silkscreen next to power connections
- Put max current on the silkscreen next to power connections
- Put version text on the silkscreen
- Add more (ground) test pads
- Round all pcb corners
- Place M4 mounting holes on diagonal ends of the PCB or preferrably in all 4 corners
- More. Ground. Testpads.
- Use 0603 SMD components wherever possible
- Try to use E12-series resistor, capacitor and inductor values
- Create a BOM containing at least the part's reference designator, part name/number and resistance/capacitance value
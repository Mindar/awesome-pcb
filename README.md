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
- **LM317T** linear power supply, widely available and known
- **‎W25Q series** SPI flash memory
- **‎STM32F103C8T6** Cheap microcontroller, same as on bluepills, 48 Mhz, ADC, I<sup>2</sup>C, SPI, USB
- **STM32F417** Bigger and faster alternative for the F103, F417/F427 have crypto hardware, F407 does not, 168 Mhz, ADC/DAC, I<sup>2</sup>C, SPI, USB, Ethernet
- **STM32F767** Bigger and even faster than the F417, Nucleo Board available
- **‎FQP30N06L** Logic Level Mosfet V<sub>DSS</sub> 60V, I<sub>D</sub> 32A, R<sub>on</sub> 35mOhm, V<sub>gs<sub>th</sub></sub> < 2.5V, around 10A @ 3.3V V<sub>gs</sub>
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
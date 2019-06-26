# Awesome PCB
This list contains awesome pcb-design related things.

## Content
- [ICs and Components](#ICs\ and\ Components)
- [PCB Manufacturing](#PCB\ Manufacturing)
- [PCB Assembly](#PCB\ Assembly)

## ICs and Components
- **LM317T** linear power supply, widely available and known
- **‎W25Q series** SPI flash memory

## Part shops
- [Digikey](https://digikey.com) they have pretty much everything, US based
- [LCSC](https://lcsc.com) very cheap and good assortment of parts, from China

## PCB Manufacturing
- [PCB Shopper](https://pcbshopper.com/) compares many pcb manufacturers
- [JLCPCB](https://jlcpcb.com/) 2$ for 10 PCBs
- [Elecrow](https://www.elecrow.com/services.html)
- [Seeed](https://www.seeedstudio.com/fusion.html)

## PCB Assembly
- [PCB Shopper](https://pcbshopper.com/) compares many pcb assemblers
- [Elecrow](https://www.elecrow.com/services.html)
- [Seeed](https://www.seeedstudio.com/fusion.html)

## PCB Design guidelines/recommendations
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
# Awesome PCB
This list contains awesome pcb-design related things.
If you know some cool thing that's related to PCB design, feel free to add it. Pull requests welcome.

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
- **LT1767** Monolithic 1.5A Step Down Regulator, 1.25 Mhz Switching frequency, Fixed output voltages of 1.8V, 2.5V, 3.3V and 5V, 2% output tolerance
- **HT7333/HT7833** Battery-friendly LDO (low Iq)
- **LM1117** One of most popular "jellybean" SMD LDO, available from many vendors
- **TPS61021** Step-up that can work from single cell (up to 1.5A)
- **TLV61220** Step-up that can work from single cell (more efficient, but less current)
- **ME7660** Cheap charge pump for negative rail (opamp, analog switches, etc)

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
- **IRFP260** Really super enormously beefy Mosfet. Suitable for linear operation, e.g. in electronic loads. TO-247 package
- **FQL40N50** Linear Mosfet, but even beefier than the IRFP260
- **KIA50N03/KIA50N06** Very cost efficient beefy (30/60V and 50A!) and reasonably low Rds(on) N-FET in DPAK case


### <a name="components_mosfet"></a>RF Parts
- **ADL5544** Wideband RF gain block, 30 MHz - 6 GHz, fixed gain of 17.4 dB
- **SKY13345-368LF**  0.1-3.5 GHz SP3T Switch
- **AS211-334** 0.1 to 4.0 GHz pHEMT SPDT Switch

### <a name="components_opamp"></a>Operational Amplifiers
- **LM358** Simple dual OpAmp, not great, not terrible
- **OPA2206** ±40V Precision OpAmp, similar to LM358, but better in every way
- **LMV611** Rail-2-Rail OpAmp up to +5V
- **OPA2277** Dual Precision OpAmp, 10µV Offset, 0.1µV/°C Drift, +36V/±18V Supply Range, affordable at ~1€

### <a name="components_sensors"></a>Sensors
- MCP9700 Temperature Sensor

### <a name="components_connectors"></a>Connectors
Distributors sell all sorts of connectors. There is a special connector for almost any application you could think of. However most of the time you don't need anything special, you just need something that works. Often a simple pin header/socket does the job. But sometimes your applicaiton is just a tiny bit more demanding. The connectors in this category fulfil such purposes. They're not special-purpose, but they do have some advantages over regular pin headers.
- **Molex 6410 Series** PCB pin headers (mates with **2695 Series** connectors) are polarized connectors that are somewhat compatible with pin headers (both have a 2.54mm spacing). If you use both socket and connector you can't plug things in the wrong way. Connector Part Number: 22012xx1 where xx is the number of pins e.g. 04 to get 4 Pins. Pin header part number is 22272xx1, where xx is the number of pins.
- **Ningbo Kangnex Elec WJ15EDGK-3.81 Series** They are pluggable screwterminals and can deal with quite a bit of current (5A and more per pin). They are also polarized so plugging them in the wrong way is impossible. The PCB-side receptacle is called WJ15EDGRC-3.81-4P, where 4P gives the number of pins (4 in this case). The screw-terminal-plug is called WJ15EDGK-3.81-4P. Once again the 4P means 4 pins. They are also availble in right-angle versions (WJ15EDGVC-3.81-4P and WJ15EDGKA-3.81-4P). There is also a version that can be locked in place with screws (WJEDGKM-3.81-4P and WJ15EDGRM-3.81-4P). They are available in many pin counts at lcsc.com. Phoenix Contact (and many other companies) has a similar product, but their product numbering sucks, so it isn't listed here.



### <a name="components_other"></a>Miscellaneous
- NHD-12232KZ-NSW-BBW-P Graphic LCD, 128x32 Pixels, fairly cheap ~14€, similar form factor to 16x2 text LCDs, 8800/6800 compatible

##  <a name="shops"></a>Part shops
- [Digikey](https://digikey.com) they have pretty much everything, US based
- [LCSC](https://lcsc.com) very cheap and good assortment of parts, from China
- [Mouser](https://mouser.com) another distributor
- [Farnell](https://de.farnell.com) another distributor
- [RS Components](https://www.rs-online.com) They also sell lots of mechanical parts such as motors, industrial automation equipment, etc

## <a name="manufacturing"></a>PCB Manufacturing
- [PCB Shopper](https://pcbshopper.com/) compares many pcb manufacturers
- [JLCPCB](https://jlcpcb.com/) Super affordable PCBs from China, multiple colors including matte black, 2$ for 5 PCBs
- [Aisler](https://aisler.net/) High Quality PCBs from Germany
- [Oshpark](https://oshpark.com/) High Quality PCBs from the US, "After Dark" style, can do Flex-PCB at $10/square inch
- [Elecrow](https://www.elecrow.com/services.html)
- [Seeed](https://www.seeedstudio.com/fusion.html)
- [PCBWay](pcbway.com)

## <a name="assembly"></a>PCB Assembly
- [PCB Shopper](https://pcbshopper.com/) compares many pcb assemblers
- [JLCPCB](https://jlcpcb.com/)
- [Elecrow](https://www.elecrow.com/services.html)
- [Seeed](https://www.seeedstudio.com/fusion.html)
- [PCBWay](pcbway.com)


## <a name="software"></a>EDA Software
- [KiCAD](http://kicad.org/) free and open source EDA software, had some pretty big updates and improvements recently
- [geda](http://pcb.geda-project.org/) free and open source
- [Fritzing](https://fritzing.org/) free and open source if you compile it yourself. A binary download costs 9 €.
- [EAGLE](https://www.autodesk.de/products/eagle/free-download) free for smaller boards
- Target 3001! not open source, but free for small personal boards
- Altium Designer, not free or open source
- Orcad, not free or open source
- [TopoR](https://www.eremex.com/products/topor/) Free license for small boards of hobbyists, very funny curvy traces autorouter

## <a name="guidelines"></a>PCB Design guidelines/recommendations
Please note that the following guidelines/recommendations are the result of my own experience designing pcbs.
- Add test pads or preferably actual test-pins for power, ground and important signals
- Mark important test pins with a descriptive name if possible (e.g. "temperature", "V_out", "threshold set")
- mark all pin names on the PCB
- mark all important connectors, e.g. "Sensor-Input", "UART", "I2C", even obvious things such as "USB"
- mark polarity of all polarized components such as diodes, connectors, electrolytic capacitors
- add 3 fiducials for better PCBA using computer vision, worst case 2 is sufficient
- clearly mark pin 1 of all ICs and connectors, preferably additionally mark IC footprints the same way the IC itself is marked (e.g. chamfered edges or pin 1 marking)
- Put reference designators for every component on the PCB if you have the space. Otherwise create a pdf or printout of the board that contains reference designators.
- Don't use text smaller than 0.8mm
- Add more test pads for ground (and other voltages/signals)
- Put polarity icon(s) on the silkscreen next to power connections. In particular Barrel Jacks.
- Put minimum and maximum input/output voltage on the silkscreen next to power connections. E.g. "12-24 VDC" or "48 VAC". If you have tighter voltage tolerances than 10% add it to the silkscreen.
- Put max current draw or max current sourcing capability on the silkscreen next to power connections. e.g. "3A"
- Put version number and date on the silkscreen. E.g. "v1.0 November 2020" or "V2 07/2015"
- Add even more ground test pads
- Round all external pcb corners to prevent injury. Your PCB **WILL** be handled by humans at some point. Don't skimp on this. Any injuries from sharp edges will be your fault.
- Depending on PCB size and weight, place M2.5, M3 or M4 mounting holes on opposite ends of the PCB or preferrably in all 4 corners
- More. Ground. Testpads.
- Use 0603 SMD components whereiver possible for automated assembly.
- avoid traces under components (risk of short due silkscreen wearout during prototyping/rework) which is hard to debug, interference
- Try to use E12-series resistor, capacitor and inductor values first, bevore going to E24, E48, etc.
- Create a BOM containing each part's reference designator, part name/number and resistance/capacitance value, manufacturer part number, seller link
- When designing break-away sections, use a slot of at least 2mm width, for tabs add mousebites/vias **in line with the board edge** do not recess them into the board. Make sure whoever breaks it sands it down.
- Create at least an A4 summary documentation, which should include a picture of the assembled board.
- For microcontroller boards add a UART/JTAG/SWD pinout for debugging somewhere on the board

## Status LEDs
- Make LEDs as dark as possible and as bright as necessary. Status LEDs should not be bright enough to illuminate anything, only bright enough to recognize they're on.
- Status LEDs should emit diffuse light, if possible add a diffusor like milky-white acrylic glass to your enclosure
- Add a power LED that shows when the device is receiving power
- Add red LEDs that indicate devices that record things such as video, audio or GPS tracks. Bonus points for devices that record other data such as acceleration data, voltage, current and others. Continuous red means its recording.
- Don't let LEDs blink unless there is a fault. Faults should always be indicated by blinking LEDs. One exception to this guideline are status LEDs for things like UART TX/RX line or Ethernet Connections.

|Color|Meaning|
|---|---|
|green (continuous)| - status is nominal<br>- device/function is turned on |
|yellow (continous)| - abnormal status<br>- device pausing abnormally<br>- possible fault indication<br>- warning|
|red (continuous)| - camera/microphone/device is recording<br>- error state, immediate attention is **not** required |
|red (blinking)| - device is stopped or stopping due to critical fault (e.g. emergency stop was pressed). Immediate Attention is required.|

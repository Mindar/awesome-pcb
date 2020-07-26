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
+**LT1767** Monolithic 1.5A Step Down Regulator, 1.25 Mhz Switching frequency, Fixed output voltages of 1.8V, 2.5V, 3.3V and 5V, 2% output tolerance

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

##  <a name="shops"></a>Part shops
- [Digikey](https://digikey.com) they have pretty much everything, US based
- [LCSC](https://lcsc.com) very cheap and good assortment of parts, from China

## <a name="manufacturing"></a>PCB Manufacturing
- [PCB Shopper](https://pcbshopper.com/) compares many pcb manufacturers
- [JLCPCB](https://jlcpcb.com/) Super affordable PCBs from China, multiple colors including matte black, 2$ for 5 PCBs
- [Aisler](https://aisler.net/) High Quality PCBs from Germany
- [Oshpark](https://oshpark.com/) High Quality PCBs from the US, "After Dark" style, can do Flex-PCB at $10/square inch
- [Elecrow](https://www.elecrow.com/services.html)
- [Seeed](https://www.seeedstudio.com/fusion.html)

## <a name="assembly"></a>PCB Assembly
- [PCB Shopper](https://pcbshopper.com/) compares many pcb assemblers
- [JLCPCB](https://jlcpcb.com/)
- [Elecrow](https://www.elecrow.com/services.html)
- [Seeed](https://www.seeedstudio.com/fusion.html)

## <a name="software"></a>EDA Software
- [KiCAD](http://kicad-pcb.org/) free and open source EDA software, had some pretty big updates and improvements recently
- [geda](http://pcb.geda-project.org/) free and open source
- [EAGLE](https://www.autodesk.de/products/eagle/free-download) free for smaller boards
- Altium Designer, not free or open source
- Orcad, not free or open source

## <a name="guidelines"></a>PCB Design guidelines/recommendations
Please note that the following guidelines/recommendations are the result of my own experience designing pcbs.
- Add test pads for power, ground and important signals
- Put pin names on the PCB
- Put reference designators for every component on the PCB
- Don't use text smaller than 0.8mm
- Add more test pads for ground (and other voltages/signals)
- Put polarity icon(s) on the silkscreen next to power connections
- Put min and max voltage on the silkscreen next to power connections
- Put max current on the silkscreen next to power connections
- Put version text on the silkscreen
- Add even more ground test pads
- Round all pcb corners
- Place M4 mounting holes on diagonal ends of the PCB or preferrably in all 4 corners
- More. Ground. Testpads.
- Use 0603 SMD components wherever possible
- Try to use E12-series resistor, capacitor and inductor values
- Create a BOM containing at least the part's reference designator, part name/number and resistance/capacitance value
- When designing break-away sections, use a slot of at least 2mm width, for tabs add mousebites/vias in line with the board edge
- Create at least an A4 summary of the documentation

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
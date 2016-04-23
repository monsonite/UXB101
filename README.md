# UXB101

#Universal Expansion Board 101

For some months I have been creating new designs using a 50mm x 50mm standard shield format - which adds an extra 8 pins to the familiar Arduino shield, and constrains it to just 50 x 50 mm - for minimum manufacturing cost by some of the Far Eastern pcb manufacturers.

The 50x50 format has worked out well for small designs, but the time has come to extend it - particularly in the requirement of larger pin-count microcontroller and FPGA devices. At the same time I wanted to keep it nominally compatible with Arduino and Arduino MEGA - because of the vast number of shields and other boards that utilise these formats.

So I have added some extra at either end to make a 50mm x 101.5mm board (approx 2" x 4") - that has a much greater pin count and increased area for circuitry. It retains Arduino and MEGA compatibility and provides an additional 26 pins more than the Arduino MEGA format.

The name UXB-101 comes from "Universal Expansion Board" 101mm long and that there are 101 useful signals.

#Details of Pin Out

The board has 6 generic 16 bit ports labelled A to F - these have been derived from the Arduino naming

Port A   Analogue
Port D   Digital

For the Port C and D headers, the following suggestions loosely apply.

Port  C  Communications  (UARTs, SPI, I2C etc)
Port  B  "Buttons"

To which I have added E and F  - which are the additional signals found in the double row header at the end of the pcb.

Ports E and F are ideally suited for bus applications - where large numbers of signals need to be connected between a series of stacked or backplaned boards. Applications might include 16 address and 16 data lines,  R,G, B digital video plus sync &amp; control lines, HDMI data etc.

To accompany these "backplane" connectors, there are 4 "Identity" pins  I0 - I3  - these may be used to connect an eeprom or other means of identifying the shield.  They are located at the very bottom of the 2 row header - in a location not used by the MEGA. They could be used as a board select address - allowing one of 16 boards to be selected in a backplane.

5V and 0V accompany the backplane - and it would be likely that each board would have its own 3V3 regulator to step the 5V down to the required level.


In this repository are the .sch and .brd files for UXB101 created using EagleCAD 6.50. Feel free to incorporate into new designs and share.

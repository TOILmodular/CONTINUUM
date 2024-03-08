# BOM

| Description | Value | Quantity | |
| --- | --- | --- | --- |
| Resistor 1/4W | 470R | 8 | |
| Resistor 1/4W | 510R | 4 | |
| Resistor 1/4W | 1K | 11 | |
| Resistor 1/4W | 3.3K | 4 | |
| Resistor 1/4W | 4.7K | 4 | |
| Resistor 1/4W | 10K | 24 | |
| Resistor 1/4W | 20K | 12 | |
| Resistor 1/4W | 22K | 8 | |
| Resistor 1/4W | 30K | 9 | |
| Resistor 1/4W | 33K | 16 | |
| Resistor 1/4W | 39K | 8 | |
| Resistor 1/4W | 47K | 21 | |
| Resistor 1/4W | 100K | 37 | |
| Resistor 1/4W | 200K | 1 | |
| Resistor 1/4W | 1M | 8 | |
| Capacitor Electrolytic | 22uF | 2 | |
| Capacitor Electrolytic | 1uF | 4 | |
| Capacitor Ceramic | 0.1uF | 28 | SMD (1608) |
| Capacitor Ceramic | 1000pF | 4 | |
| Capacitor Ceramic | 560pF | 4 | |
| Capacitor Ceramic | 100pF | 4 | |
| Diode | 1N5819 | 2 | |
| Diode | 1N5817 | 4 | |
| LED | 3mm | 20 | See section "Choice of resistors for LEDs" below |
| Op Amp | TL074 | 8 | |
| Op Amp | TL071 | 1 | |
| Quad VCA | AS2164 or V2164 | 1 | |
| Potentiometer | B100K | 4 | |
| Potentiometer | B10K | 4 | |
| Potentiometer | B5K | 4 | |
| Potentiometer | B1K | 5 | |
| Mono Jack | 3.5mm | 5 | |
| Switch | Toggle SPDT | 4 | ON-ON |
| Switch | Toggle SPDT | 4 | ON-OFF-ON |
| Header | 2.54mm L-shape Male 1x5 | 1 | Connector Front Panel Touchpads |
| Header | 2.54mm Female 1x5 | 1 | Connector Control Board Touchpads |
| Header | 2.54mm Male 1x8 | 3 | Connector Main Board |
| Header | 2.54mm Male 1x7 | 1 | Connector Main Board |
| Header | 2.54mm Female 1x8 | 3 | Connector Control Board |
| Header | 2.54mm Female 1x7 | 1 | Connector Control Board |
| Header | 2.54mm Male 2x5 | 1 | Power Connector |

## Choice of resistors for LEDs
The module contains a line of 20 LEDs at the front panel with five LEDs in a row representing one oscillator above them.

I tried out a lot of different values for the resistors in the vicinity of each LED to get a certain effect, so that the volume of each oscillator is visualized by the row of five LEDs, with the central LED the brightest, and neighboring LEDs slightly less bright. 
Each LED brightness is defined by three resistors, e.g. R46, R51, and R136 (in the schematic) for the most left-side LED.

The resistors connected between the incoming CV signal from the VCA and the LEDs (in the example R46) are given on the control PCB directly above the line of LEDs with values 39K (least bright) - 30K (middle bright) -20K (brightest) - 30K - 39K for one group of five LEDs for one oscillator.

There is another 47K resistor connected between each LED and the -12V power supply (in the example R51).
You will find those resistors on the right side of each LED on the PCB.

Finally, there is one more resistor between each LED and ground (in the example R136).
The five values for that resistor in each group are 15K (least bright) - 20K (middle bright) -100K (brightest) - 20K - 15K.
Those resistors are on the left side of each LED on the PCB.

All those values have been chosen just via breadboard tests.
The LEDs in my module, for which those resistor values work out ok, are blue ones (470nm, forward voltage 3.1V, current 35mA, product number OSB5DL3E34B).

You might have to play around with those resistor values, depending on the used LEDs and the desired brightness differences.


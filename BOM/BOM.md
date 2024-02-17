# BOM

| Description | Value | Quantity | |
| --- | --- | --- | --- |
| Resistor 1/4W | 100R | 4 | |
| Resistor 1/4W | 470R | 8 | |
| Resistor 1/4W | 510R | 4 | |
| Resistor 1/4W | 1K | 21 | |
| Resistor 1/4W | 3.3K | 4 | |
| Resistor 1/4W | 4.7K | 12 | |
| Resistor 1/4W | 10K | 24 | |
| Resistor 1/4W | 12K | 4 | |
| Resistor 1/4W | 22K | 8 | |
| Resistor 1/4W | 30K | 1 | |
| Resistor 1/4W | 33K | 16 | |
| Resistor 1/4W | 47K | 5 | |
| Resistor 1/4W | 100K | 33 | |
| Resistor 1/4W | 200K | 1 | |
| Resistor 1/4W | 1M | 8 | |
| Resistor 1/4W | LED1 | 4 | See footnote *) |
| Resistor 1/4W | LED2 | 8 | See footnote *) |
| Resistor 1/4W | LED3 | 8 | See footnote *) |
| Capacitor Electrolytic | 22uF | 2 | |
| Capacitor Electrolytic | 1uF | 4 | |
| Capacitor Ceramic | 1uF | 4 | |
| Capacitor Ceramic | 0.1uF | 18 | SMD (1608) |
| Capacitor Ceramic | 0.022uF | 4 | |
| Capacitor Ceramic | 1000pF | 4 | |
| Capacitor Ceramic | 560pF | 4 | |
| Capacitor Ceramic | 100pF | 4 | |
| Diode | 1N5819 | 2 | |
| Diode | 1N5817 | 4 | |
| LED | 3mm | 20 | |
| Transistor | MMBT3904 | 4 | SMD (SOT-23-3) |
| Op Amp | TL074 | 7 | |
| Op Amp | TL071 | 1 | |
| Quad VCA | AS2164 or V2164 | 1 | |
| Potentiometer | B100K | 4 | |
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

*) Resistors "LED1" - "LED3" are pull-down resistors for the 20 LEDs.
The resistor values depend on the used LEDs and the desired brightness.
The row of LEDs is divided in four groups, each with five LEDs, representing the CV level applied to the VCA for each oscillator section above the LEDs.
I chose the values in a way that the central LED of each group is the brightest (resistors "LED1"), the two LEDs next to it are a bit less bright (resistors "LED2"), and the two next to those are the least bright ones (resistors "LED3").
The values for that effect with blue LEDs in my module are: LED1 = 47K, LED2 = 100K, LED3 = 470K. 

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
| Potentiometer | B1K | 1 | |
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

All those values have been chosen just via breadboard tests.
The LEDs in my module, for which those resistor values work out ok, are blue ones (470nm, forward voltage 3.1V, current 35mA, product number OSB5DL3E34B).

You might have to play around with those resistor values, depending on the used LEDs and the desired brightness differences.

<img width="233" src="https://github.com/TOILmodular/CONTINUUM/assets/97026614/7e90ba08-6317-4c5b-a54e-30b074de8120">

The resistors between the incoming CV signal from the VCA and the LEDs can be found on the control PCB in four groups with five resistors above the line of LEDs with values 20K (e.g. R46 in the schematic) - 20K (R47) - 10K (R48) - 20K (R49) - 20K (R50) for one oscillator.

<img width="500" src="https://github.com/TOILmodular/CONTINUUM/assets/97026614/eb47e263-8093-47ec-84a6-fa16b65028bd">

There is another resistor connected between each LED and the -12V power supply.
The values for those resistors in each group are 47K (e.g R51) - 47K (R52) - 22K (R53) - 47K (R54) - 47K (R55).
You will find those resistors on the right side of each LED on the control PCB.

<img width="500" src="https://github.com/TOILmodular/CONTINUUM/assets/97026614/f674f779-55f1-4751-bcb9-1444b6d48a52">

Finally, there is one more resistor between each LED and ground.
The five values for that resistor in each group are 47K (e.g. R136) - 470K (R135) - 470K (R134) - 470K (R57) - 47K (R56).
Those resistors are on the left side of each LED on the PCB.

<img width="500" src="https://github.com/TOILmodular/CONTINUUM/assets/97026614/e406a704-17ce-4738-9899-5cb3c95d86d5">

I decided to use resistors only, and no transistors (which I guess would be the usual way to control LEDs), because I wanted to have some control over the LED brightness, depending on the CV - and therefore the volume - of each oscillator.
There might be a more elegant way to do that, but I wanted to keep the design simple in terms of used components.
This combination of resistors for incoming CV, additional negative voltage (the CV controlling the VCA in the AS2164 is actual negative), and ground turned out to get the right amount of current for the desired effect.
Disadvantage is that the values will not be the right ones for other LEDs.

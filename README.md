# CONTINUUM - a 4-oscillator drone Eurorack module
This Eurorack module provides a drone from four oscillators with volume modulation controls for each oscillator via touch pads, internal or external CV.

<img height="500" src="https://github.com/TOILmodular/GARGLER/assets/97026614/3fb18a32-90c7-4129-8e60-ad567214e95c">
<img height="500" src="https://github.com/TOILmodular/GARGLER/assets/97026614/2d934e23-873a-4cbc-9ae3-71b2fb08ed65">

<img height="500" src="https://github.com/TOILmodular/GARGLER/assets/97026614/121e99c1-6281-40e6-89a4-87d81681f247">
<img height="500" src="https://github.com/TOILmodular/GARGLER/assets/97026614/da834276-f82b-410b-8704-74eb76ab6ea8">


#### Features
- Four separate oscillator segments
- Triangle or squarewave selection
- Three different volume modulation options - external, internal (irregular, cyclic via LFO combinations), or touch pads at the front panel
- Simple low-pass filter function for squarewave mode for morphing between square and shark fin waveform
- Volume control for the summed up output signal

A demo of the module is available in this YouTube video:

[<img width="500" src="https://github.com/TOILmodular/GARGLER/assets/97026614/70f6cd10-a251-469a-80bf-59df53929b95">](https://youtu.be/kjN41rJ36m0)

## How the Module works
The four oscillator sections are identical.

#### FREQUENCY
The FREQUENCY knob determines the pitch of each oscillator.
This is a simple drone module with no CV for the pitch.

#### Waveform Switch
There are two options for each oscillator's waveform via the toggle switch next to the FREQUENCY knob - triangle or squarewave.

#### CV Controls
The module contains a quad VCA for modulating the volume of each oscillator. There are three CV options for each VCA.
The options for internal and touch pad modulation can be selected via a toggle switch.
Positioning the switch at the center interrupts any modulation signal to be sent from internal or touch pad to the VCA.

##### Internal CV
The module provides an internal modulation of each VCA via four internal LFOs, which are being combined differently for each oscillator and used for the volume modulation.
Therefore, those modulations are irregular but cyclic.

##### Touch Pads
There are two touch pad sections at the bottom of front panel, which are based on a simple mechanism using the conductivity of fingers placed on the pads. Select that option for an oscillator by pushing the related toggel switch down. The pads are also slightly pressure sensitive. So the CV level can be controlled by pressure, but also by the size of the area covered by the fingers. The set of pads on the left are controlling the left two oscillators, the pads on the right are for the other two oscillators on the right.

##### Internal Modulation
Pushing the modulation option switch up, will cause the VCA of the related oscillator volume to be modulated by a certail pattern created by the combination of two internal LFOs with different rates. That pattern is different for each oscillator.

##### External CV
There is a CV input for each oscillator section. Touch pad and internal CV are normalled to this input. I.e. as long as there is a cable plugged in to the CV input, the only VCA modulation will be from an external source.

#### BIAS
The BIAS knob provides a CV offset option for the VCA modulation. This is applied to any of the above described options.
You can turn down the output from any oscillator separately with the BIAS turned to minimum and no CV signal added.

#### FILTER
The FILTER knob is only functional in case the selected waveform of an oscillator is the squarewave. In that case, it is serving as a simple low-pass filter, morphing the squarewave into a shark fin.

#### VOLUME
The volume knob is controlling the overall amplitude of the combined drone output.

#### OUT
The combined output of all four oscillators.

## Module Build and PCBs
I added two different versions for the control board in the folder GerberFiles, an "original", and a "Thonk" version.
Reason is that for my own module, I am using specific potentiometers - 16K4 series from Supertech Electronics - and 3.5mm jack sockets - MJ-355 from Marushin - available at my local electronics shop.

<img width="300" alt="CtrlPCB_Orig" src="https://github.com/TOILmodular/CONTINUUM/assets/97026614/dc18885e-3439-4b7f-a738-9cde5bdc44a2">

However, since most DIY projects for Eurorack modules out there are using potentiometers from ALPHA and so-called THONKICONN jacks, as they are provided by Thonk in the UK, I also created another control board PCB for the "Thonk" version with footprints for those components.

<img width="300" alt="CtrlPCB_Thonk" src="https://github.com/TOILmodular/CONTINUUM/assets/97026614/6617db9b-e79d-4699-a843-b4237903a712">

The main PCB is the same for both versions.

<img width="300" alt="MainPCB" src="https://github.com/TOILmodular/CONTINUUM/assets/97026614/516773c2-40f5-4bf4-808b-1cef77f619c8">

I created the Gerber files with the online tool EasyEDA and ordered the PCBs at JLCPCB.

## Panel Layout
I added the information about hole coordinates for the front panel in the folder PanelLayout, referring to the component layout in the PCB Gerber files.

In addition, there is another Gerber file for the panel, following the HP standard. My own modules do not follow that width standard, as I am only using sliding nuts in my racks.

You can use the panel Gerber file to have the panel built out of PCB material.

## Additional Information about specific Components
The module build is mainly THT, including all ICs.
However, there are a few SMD components if you are using the Gerber files provided.

There are a number SMD capacitors with the package size 1608 (imperial 0603), as well as several NPN transistors MMBT3904 with package size SOT-23-3.

Concerning the resistor size, I am usually using small-size resistors, about half the length of the usual size, so they need less space on the PCB. If you want to use my Gerber files, you have to consider that fact. You might still use normal size resistors and put them in a standing position on the boards. Should also work fine.

## Soldering ICs on Control Board
There are three ICs to be soldered on the control board in a special way, although the ones to be used are THT.
Due to space reasons, there are no holes for the IC sockets.
The socket legs need to be soldered to the PCB surface, like SMD components.

In order to do that, you need to use those types of sockets, where the legs can be bent, NOT the ones with stiff round legs!

<img width="500" src="https://github.com/TOILmodular/GARGLER/assets/97026614/440ea4bd-f64a-49aa-b3e9-e93ae8265c44">

All socket legs need to be bent to the outside, so they can be put flat onto the PCB. Soldering a socket to the board is very easy, since the legs and the space inbetween are big compared to real SMD components.

<img width="500" src="https://github.com/TOILmodular/GARGLER/assets/97026614/437a25b2-b9cc-4be9-bf65-0ad2c10efac4">
<img width="500" src="https://github.com/TOILmodular/GARGLER/assets/97026614/31184858-4c74-43f4-b11a-abf582f29de1">

The sockets on the main board are to be soldered the usual THT way.

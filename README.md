# CONTINUUM - a 4-oscillator drone Eurorack module
This Eurorack module provides a drone from four oscillators with volume modulation controls for each oscillator via touch pads, internal or external CV.

<img height="500" src="https://github.com/TOILmodular/CONTINUUM/assets/97026614/9aa25208-d464-4d61-b3e9-2e5df699201f">
<img height="500" src="https://github.com/TOILmodular/CONTINUUM/assets/97026614/58ca1409-5d84-451c-b231-6b8a6a3aa704">
<img height="500" src="https://github.com/TOILmodular/CONTINUUM/assets/97026614/e4c4f242-04d6-43ca-b9a0-35b27e8f3371">

#### Features
- Four separate oscillator segments
- Triangle or squarewave selection
- Three different volume modulation options - external, internal (irregular, cyclic via LFO combinations), or touch pads at the front panel
- Volume indicators via LEDs for each oscillator
- Simple passive low-pass filters for each oscillator
- Volume control for the summed up output signal
- Module width 26HP

A demo of the module is available in this YouTube video:

[<img width="500" src="https://github.com/TOILmodular/CONTINUUM/assets/97026614/49dcf8b2-ba21-4d22-ade6-f03891f9c837">](https://youtu.be/6xKqU5N0I0M)

## How the Module works
The four oscillator sections are identical, except for the internal modulation LFO combinations.

#### FREQUENCY Knob
The FREQUENCY knob determines the pitch of each oscillator.
This is a simple drone module with no CV for the pitch.

#### Waveform Switch
There are two options for each oscillator's waveform via the toggle switch next to the FREQUENCY knob - triangle or squarewave.

#### CV Controls
The module contains a quad VCA for modulating the volume of each oscillator. There are three CV options for each oscillator's VCA.
The options for internal and touch pad modulation can be selected via a toggle switch.
Positioning the switch at the center interrupts any modulation signal to be sent from internal or touch pad to the VCA.

##### Modulation Option 1: Touch Pads
There are two touch pad sections at the bottom of the front panel, which are based on a simple mechanism using the conductivity of fingers placed on the pads.
Select that option for an oscillator by pushing the related toggle switch down.
The pads are also slightly pressure sensitive.
So the CV level can be controlled by pressure, but also by the size of the area covered by the fingers.
The set of pads on the left are controlling the left two oscillators, the pads on the right are for the other two oscillators on the right.
The sensitivty of the pads is very much depending on how wet your fingers are.
If you wet your fingers slightly, the volume of the oscillators is increasing much faster, than with dry fingers.

##### Modulation Option 2: Internal Modulation
Pushing the modulation option switch up, will cause the VCA of the related oscillator to be modulated by a certain pattern created by the combination of two internal LFOs. That pattern is different for each oscillator, as the module contains four separate LFOs with different fixed rates.

##### Modulation Option 3: External CV
There is a CV input for each oscillator section. Touch pad and internal CV are normalled to this input. I.e. as long as there is a cable plugged in to the CV input, the only VCA modulation will be from an external source.
The setting of the modulation option toggle switch will have no influence in this case.

#### BIAS Knob
The BIAS knob provides a CV offset option for the VCA modulation. This is applied to any of the above described options.
You can turn down the output from any oscillator separately with the BIAS turned to minimum and no CV signal added.
Or you can ensure to have a constant tone with slight volume modulation on top by increasing the bias to a certain amount.

#### FILTER Knob
The FILTER knob is to control the cutoff frequency of a simple passive low-pass filter with no resonance.

#### VOLUME Knob
The volume knob is controlling the overall amplitude of the combined drone output.
You might get a signal clipping, when turning it to max and having more than one oscillator playing.
So this is another way of influencing the output signal.

#### OUT
The combined audio signal from all four oscillators.

## Module Build and PCBs
I added two different versions for the control board in the folder GerberFiles, an "Original", and a "Thonk" version.
Reason is that for my own module, I am using specific potentiometers - 16K4 series from Supertech Electronics - and 3.5mm jack sockets - MJ-355 from Marushin - available at my local electronics shop.

<img width="300" alt="CtrlPCB_Orig" src="https://github.com/TOILmodular/CONTINUUM/assets/97026614/c098f5e1-8d5e-4a9e-874e-4ce69e2a1384">

However, since most DIY projects for Eurorack modules out there are using potentiometers from ALPHA and so-called THONKICONN jacks, as they are provided by Thonk in the UK, I also created another control board PCB for the "Thonk" version with footprints for those components.

<img width="300" alt="CtrlPCB_Thonk" src="https://github.com/TOILmodular/CONTINUUM/assets/97026614/7407211b-bb3d-4ddc-9a96-8bd26ed4a077">

The main PCB is the same for both versions.

<img width="300" alt="MainPCB" src="https://github.com/TOILmodular/CONTINUUM/assets/97026614/14a2d77e-8bc3-4a48-a3fd-768e2b902dcf">

I created the Gerber files with the online tool EasyEDA and ordered the PCBs at JLCPCB.

## Additional Information about specific Components
The module build is mainly THT, including all ICs.
However, there are a number of SMD capacitors with the package size 1608 (imperial 0603).

For the "Original" version one of the IC sockets on the control board needs to be soldered in a specific way, as described in the next section. For the "Thonk" version, all sockets are to be soldered the usual way.

Concerning the resistor size, I am usually using small-size resistors, about half the length of the usual size, so they need less space on the PCB. If you want to use my Gerber files, you have to consider that fact. You might still use normal size resistors and put them in a standing position on the boards. Should also work fine.

## Soldering IC Sockets on Control Board (only valid for the "Original" PCB version!)
The following information is not relevant, if you are using the "Thonk" version PCBs.

There is one 8-pin IC socket to be soldered on the control board in a special way, although the TL071 IC themself is THT.
Due to space reasons, there are no holes for the IC socket.
The socket legs need to be soldered to the PCB surface, like SMD components.

In order to do that, you need to use the type of socket, where the legs can be bent, NOT the one with stiff round legs!

<img width="500" src="https://github.com/TOILmodular/CONTINUUM/assets/97026614/fe262cfd-d46b-4282-a18c-44e215a4d713"> 

All socket legs need to be bent to the outside, so they can be put flat onto the PCB. Soldering the socket to the board is very easy, since the legs and the space inbetween are big compared to real SMD components.

<img width="500" src="https://github.com/TOILmodular/CONTINUUM/assets/97026614/b4e5d8eb-5811-49a1-ae51-4d7d5a5b1c87">
<img width="500" src="https://github.com/TOILmodular/CONTINUUM/assets/97026614/4fc33774-cd28-461e-a873-f55f07a589dd">

All other sockets on the control board and the ones on the main board are to be soldered the usual THT way.

## Front Panel and Touch Pad Connections
One thing unusual about this module is the integration of touch pads into the front panel for modulating the amount of CV to the VCA and therefore the volume for each oscillator.

Those touch pads are basically just several SMD-type solder areas connected to traces in the panel, which is actually a PCB.
Therefore, this module requires a front panel manufactured as a PCB, not e.g. an aluminum panel.
The Gerber file for that panel is available in the GerberFiles folder.

The connections for each touch pad with the control PCB are at the panel backside.
In order to connect them to the control board frontside, you have to use a 1x5 L-shaped male header, soldered on the backside surface and fitting to a corresponding 1x5 female header on the control board.

I suggest the following sequence for assembling the front panel and all control parts, and soldering the touch pad connections.
1. First finish soldering all parts on the backside of the control PCB, but not yet the control parts on the frontside (pots, jack sockets, switches, LEDs).
2. Solder the 5-pin female header to the control board.
<img width="400" src="https://github.com/TOILmodular/CONTINUUM/assets/97026614/e9f8ed89-e014-4bb7-8960-4254276c41e5">

3. Stick on the four ON-ON toggle switches at the upper row of the control board without soldering them.
4. Stick on the L-shaped male header to the female header on the control board.
<img width="400" src="https://github.com/TOILmodular/CONTINUUM/assets/97026614/38f72cde-c15b-4752-819f-fe04549c2511">

5. Put on the front panel and fix the four toggle switches with screws to the front panel.
<img width="400" src="https://github.com/TOILmodular/CONTINUUM/assets/97026614/69aa4c0d-e5ec-44ce-b7de-616c2267384e">

You can see in the picture that the control board and the front panel are not exactly parallel, because the headers connecting the touch pads are slightly higher than the switches.

6. Check the position of the L-shaped header on the backside of the front panel and gently twist it against the control PCB until the header pins fit to the solder pads.
   Then solder the header pins to the front panel.
<img width="400" src="https://github.com/TOILmodular/CONTINUUM/assets/97026614/09f35f1b-4e27-4718-ac10-771c0cfce7b1">

7. Solder the four toggle switches to the control board PCB.
8. Carefully remove the front panel, which will require disconnecting the headers for the touch pads.
9. Place all other switches, jacks, pots and LEDs.
10. Put the front panel back on. Make sure that the headers between the front panel and the control board for the touch pads are connected.
11. Fix all parts at the front panel with nuts.
12. Solder all parts on the control board.

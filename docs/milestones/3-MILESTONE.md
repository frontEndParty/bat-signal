
[PREV MILESTONE](./2-MILESTONE.md)

## MILESTONE THREE
**GOAL: TOGGLE AN LED LIGHT VIA THE CLOUD DASHBOARD**

HARDWARE SPECS:
- 1 LED
- 1 RESISTOR - VALUE: 200 - 300 OHMS
- 2 CONNECTING WIRE

<br>

<img title="3.2" alt="Attach LED and resistor to breadboard" src="../../.images/3.2.jpeg" width="400">

- ***CONNECT LED TO GROUND***
> - *the LED is polarized so current can only flow in one direction (a "diode")*
> - *if you have LED backwards it will not work*

- -> CONNECT LED'S LONG SIDE TO A TERMINAL STRIP
- -> CONNECT LEG'S SHORT SIDE TO GROUND POWER RAIL
- -> CONNECT GROUP POWER RAIL TO GROUND VIA CONNECTING WIRE
- PIN ON MCU BOARD

	<img title="3.1" alt="LED pins" src="../../.images/3.1.jpeg" width="400">

- ***CONNECT POWER AND RESISTOR TO LED***
> - *the LED cannot regulate current on its own, so we use a resistor to lower the current*
> - *without the resistor, the high current would destroy the LED*

- -> PLACE A RESISTOR PIN IN THE SAME TERMINAL STRIP AS LED PIN
- -> CONNECT OTHER RESISTOR PIN IN DIFFERENT TERMINAL STRIP
    - (*in the picture, we use the strip directly across the dip*)
- -> CONNECT STRIP ONE OF MCU BOARD'S DATA PINS VIA CONNECTING WIRE
    - (*in the picture, we use d7*)

<br>

- **CODE TASK**:
	- `SET THE MODE OF THE PIN WE ARE USING IN THE SETUP FUNCTION`
	- `USE THE EVENT LISTENER TO RESPOND TO CLOUD VARIABLE CHANGES`
		- (`if isOn` (your `bool` var) is `true` turn on LED, `else` turn off)

<br>

[NEXT MILESTONE](./4-MILESTONE.md)

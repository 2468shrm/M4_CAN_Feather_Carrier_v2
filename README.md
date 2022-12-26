# M4_CAN_Feather_Carrier_v2

![image info](./Images/Board\ Layout.png)

The carrier board is an adaptor to make using the Adafruit M4 CAN Express
Feather board more useful in FRC applications.  It provides the following:
- Power interface
  - Power comes from a 12 V supply through the provided 2-input screw terminal
  - The power supply contains a diode capacitor circuit to reduce the effects of FRC robot brownouts
- CAN interface
  - On the feather board
  - Note the feather board comes with termination included and active, so you must cut the termination trace jumper
- Analog I/O
  - 4 analog inputs
  - Buffered with a unity gain opamp
  - Proded by 3-pin interface (similar to AIO on RoboRIO)
    - Pin 1: input analog signal
    - Pin 2: 3.3V supply
    - Pin 3: Ground
  - 3.3V input, max
- Digital I/O
  - 4 digital inputs
  - Buffered with a level shifter
  - Selectable sensor voltage (VDD): 3.3V or 5V (all inputs share)
    - VDD selected by a jumper
    - 1-2 selects 3.3V
    - 2-3 selects 5V
  - Proded by 3-pin interface (similar to AIO on RoboRIO)
    - Pin 1: input analog signal
    - Pin 2: VDD supply
    - Pin 3: Ground
- Additional sensor power
	- A 2x4 header provided to provide additional VDD power to sensors
    - Intended for Adafruit beam break emitters or other multi-part sensors using an emitter and receiver pair where the receiver connects to DIO and emitter connects to the additional sensor power
- STEMMA QT/QWIIC
  - 4 interfaces provided
- Neopixel
  - A Neopixel interface provided via a 3-input screw terminal
  - Intended to allow sensor to provide state of the sensor both over CAN and visually (i.e. sensor could be disconnected while still being useful)

## Power Interface
The initial version of this board was designed at the height of the pandemic's supply
chain shortage and so while I wanted to provide a 3A 5V supply (from 12V source) finding
the components was problematic at best. So I found a cheap, simple power supply module I
could acquire on Amazon. So I used it.

## Disclaimer
While I've tested a prior version of this board, it is to be considered alpha and subject
to bugs and errors. Use at your own risk.  However the Gerbers are provided should you
want to fabricate your own.

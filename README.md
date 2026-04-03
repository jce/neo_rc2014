## Neopixel (5050 RGB LED) driver for RC2014

Documentation for a once-of project for the RC2014 computer: Driving NeoPixels on a neopixel ring. 

Driving neopixels is challenging. The RC2014 is not fast enough to achieve the waveshape for the LED's serial protocol. This driver performs a short pulse and a long pulse based on two bits in the output byte. The long pulse is achieved with an RC circuit that extends a short pulse.

The software *can* be fast enough with these output drivers. It works by first building an array of machine code that *is* fast enough when executed, and then executing that as a function.

The circuit is mostly proto board, there is no full schematic PDF. Pictures for future reference.

The ICs are: 
- 74hct688 byte comparator for address
- 74hct32 4 or ports
- 74hct04 6 inverters

The RC circuit uses 100 kOhm and 22 pF

## Pictures:
<img src="IMG_20260321_095626_768.jpg" alt="PCB front" width="600" height="400">
<img src="IMG_20260321_095642_737.jpg" alt="PCB back" width="600" height="400">
<img src="IMG_20260321_112844_994.jpg" alt="LED ring" width="600" height="400">
<img src="IMG_20260321_132459_004.jpg" alt="Whiteboard" width="600" height="400">
<img src="neo_rc2014_leds_attached.png" alt="Pulse extender scope" width="600" height="400">
# References

https://www.kiwi-electronics.com/nl/1-4-60-neopixel-ring-15-x-5050-rgb-led-met-geintegreerde-drivers-2786

https://wp.josh.com/2014/05/13/ws2812-neopixels-are-not-so-finicky-once-you-get-to-know-them/

https://z80kits.com/shop/neopixel-module-short-board/

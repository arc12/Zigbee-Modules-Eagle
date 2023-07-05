# Zigbee Modules Eagle
## E18 Simple Breakout
A simple breakout board for the Ebyte E18 MS1 "stamp" module (i.e. a version without the extra power amplifier). The device shown is the PCB variant but AFAIK the landing pattern is identical for the IPX variant.

This is "simple" in that the main use case is to plug into breadboard; although there are some components other than the E18 on the board, these are included for possible convenience (and using available board space).

Some notes:
- The long header is meant to be populated with right-angle pins. This will put the antenna nicely up and leaves plenty of space for other components on the breadboard (I find the breakouts with very wide dual-in-line pin-outs to be rather irritating, and Arduino style sockets and flying leads are not great when more than a few connections are to be made).
- The 5 pin header is for firmware flashing. I opted for this, rather than the full 10 pin "debug" header which CCLoader uses, for econonmy of space. These 5 pins are quite sufficient if using something like https://github.com/jmichault/flash_cc2531 (or my patched version for use with Pi v1 GPIOs at https://github.com/arc12/flash_cc2531).
- The 4 pin header may be convenient for either UART or I2C connections. I'm expecting to be using PTVO and for the CC2530 it fixes UART pins.
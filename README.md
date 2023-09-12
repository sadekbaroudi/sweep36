# Name

sweep36

A 36-key version of the sweep, maintaining the original diodeless PCB.

# Variations

## sweeeeep

why the name sweeeeep? Because an Elite-C is required to support the extra features, and an Elite-C has 5 additional pins... so 5 Es for the 5 extra pins. Yes, it's dumb, I know.

### Description

This is a reversible PCB that is wired only, and has per key LEDs (only on one of the two variations), OLED, and choc spacing. In order to continue to support a no-diode setup, I added support for the Elite-C, and this is now required for the build. You can use alternative Elite-C compatible controllers.

### Versions and features

There are 6 versions of this PCB, as found in the PCB/wired-rgb directory:
* choc: No hotswap, 36 keys
* choc-rotated-inner-thumb: No hotswap, 36 keys, rotated inner thumb similar to the Corne
* choc-hotswap: Hotswap only, 36 keys
* ks27-choc: Support for both choc and gateron ks-27 switches, no hotswap. Note that ks-27 switches use MX keycaps on a low profile switch. Given its choc spacing, you will likely need to use custom smaller MX keycaps if using these switches
* choc-evq-inside: No hotswap, 34 key, with an evqwgd001 roller encoder on the inside thumb key
* choc-evq-outside: No hotswap, 34 key, with an evqwgd001 roller encoder on the outside thumb key

## swweeep

So, to keep the silliness going, this has an extra W for the wireless only, and 3 Es for the 3 extra required pins on the nice!nano.

### Description (and story)

This was created after the sweeeeep as a wireless alternative. Given the nice!nano has two less GPIO than the Elite-C, had to remove the data pin (and therefore TRRS). So, this is wireless only!

Given it's a wireless only build, it made sense to add nice!view support, given it consumes 1000x less power than the typical OLED. That meant that it would consume one too many GPIO. In the spirit of low power consumption, removing per key rgb was a natural decision, leaving it with just enough GPIO for this board.

So, backstory aside, the net of it is:
* nice!nano required
* nice!view support
* wireless only (no TRRS)
* JST spaced battery through holes
* on/off switch
* Both Kailh hotswap and Mill-Max compatible through hole

Special thanks to @jasonhazel for kickstarting the initiative!

### Notes

Regarding the JST footprint, you can solder directly or use JST. If soldering, connect power to the middle hole (with the +) and GND to the -. If using JST, be sure to look at your battery wiring and connect the JST connector such that the power lines up with the middle pin (again, with the + on the silkscreen)

It is possible to also produce a PCB baseplate board for the swweeep with a nice silkscreen, the Kicad files are [here](https://github.com/sadekbaroudi/sweep36/tree/master/sweeeeep), or if you think the [Great Wave Off Kanagawa](https://en.wikipedia.org/wiki/The_Great_Wave_off_Kanagawa) would make a good silkscreen, the gerbers for that are [here](https://github.com/sadekbaroudi/sweep36/blob/master/swweeep/swweeep-base/gerber/v1.0-kanagawa-gerbers.zip)

# Support me!

I have spent a lot of time and money designing prototypes, testing, developing, etc. Any contributions would be greatly appreciated!

If you don't want to, or can't afford to support me, please send me a message to let me know you've built one, along with pictures. Also, feel free to submit a pull request with pictures into this repository. I'd be happy to showcase your build.

Reddit: /u/sadekbaroudi
Discord: sadekbaroudi#1258

[![Donate](https://img.shields.io/badge/Donate-PayPal-green.svg)](https://www.paypal.com/paypalme/sadekbaroudi)

# Firmware

## Vial (wired version only)

Special thanks to [Jason Hazel](https://github.com/jasonhazel) for adding vial support. Note that given vial with split code takes up most of the space, there is no support for the OLED or per-key RGB. If you want those features, please use QMK below.

https://github.com/sadekbaroudi/vial-qmk/tree/vial/keyboards/fingerpunch/sweeeeep

## QMK (wired version only)

https://github.com/sadekbaroudi/qmk_firmware/tree/master/keyboards/fingerpunch/sweeeeep

## ZMK (wireless version only)

https://github.com/sadekbaroudi/zmk-swweeep

# swweeep v1.3 fix

If you built a swweeep v1.3 or earlier, you will need to connect the battery ground pin to the controller GND pin, as shown below:

![pcbs](images/swweeep-v1.3-bodge.jpg)

# Pictures

## swweeep with nice!view

![pcbs](images/swweeep-1.jpg)

## swweeep with the base plate

![pcbs](images/swweeep-base.jpg)

## sweeeeep choc

![pcbs](images/sweeeeep-1.jpg)

![pcbs](images/sweeeeep-2.jpg)

![pcbs](images/pcb-kicad.png)

## sweeeeep evq inside

![pcbs](images/sweeeeep-evq-inner.png)

### sweeeeep (choc)
| Front | Back |
| :---: | :---: |
| ![front](pcb_images/sweeeeep/choc/half-swept-top.png) | ![back](pcb_images/sweeeeep/choc/half-swept-bottom.png) |

### sweeeeep (choc-evq-inside)
| Front | Back |
| :---: | :---: |
| ![front](pcb_images/sweeeeep/choc-evq-inside/half-swept-top.png) | ![back](pcb_images/sweeeeep/choc-evq-inside/half-swept-bottom.png) |

### sweeeeep (choc-evq-outside)
| Front | Back |
| :---: | :---: |
| ![front](pcb_images/sweeeeep/choc-evq-outside/half-swept-top.png) | ![back](pcb_images/sweeeeep/choc-evq-outside/half-swept-bottom.png) |

### sweeeeep (choc-hotswap)
| Front | Back |
| :---: | :---: |
| ![front](pcb_images/sweeeeep/choc-hotswap/half-swept-top.png) | ![back](pcb_images/sweeeeep/choc-hotswap/half-swept-bottom.png) |

### sweeeeep (choc-rotated-inner-thumb)
| Front | Back |
| :---: | :---: |
| ![front](pcb_images/sweeeeep/choc-rotated-inner-thumb/half-swept-top.png) | ![back](pcb_images/sweeeeep/choc-rotated-inner-thumb/half-swept-bottom.png) |

### sweeeeep (ks27-choc)
| Front | Back |
| :---: | :---: |
| ![front](pcb_images/sweeeeep/ks27-choc/half-swept-top.png) | ![back](pcb_images/sweeeeep/ks27-choc/half-swept-bottom.png) |

### swweeep (choc-hotswap-optional)
| Front | Back |
| :---: | :---: |
| ![front](pcb_images/swweeep/choc-hotswap-optional/half-swept-top.png) | ![back](pcb_images/swweeep/choc-hotswap-optional/half-swept-bottom.png) |

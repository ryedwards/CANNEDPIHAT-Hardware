# CANNEDPIHAT-Hardware
 
![CannedPiHat_3dView](https://github.com/ryedwards/CANNEDPIHAT-Hardware/blob/main/images/CannedPIHat_3DView.jpg?raw=true)

## The CannedPi Hardware
Meet the CannedPi hardware!  This simple (and not prefectly designed) Raspberry PI Hat contains an STM32G4 microcontroller which can interface with the USB port of your Pi.

Why would I create such a Rube Goldberg design??
- I wanted a HAT that would provide provide solid 5V power from a ~12V power input.  This board has a 4A SMPS that provides more than enough juice for even a power hungry Pi4.
- I wanted the option of running both scripts on the Pi (Python-CAN, C applications, etc) while also having the ability to run real-time CAN on the embedded chip as needed.
- Wanted an "all-in-one" form factor for mounting on LCD displays and other small cases
- For LIN you really need the real time microcontroller
- I wanted to prove I could do it.  Now that I feel I've achived my goal I decided to share it wth everyone

## Features
- The 26-pin header provides access to all 3 CAN channels, the LIN channel, 12V, 5V, 3.3V and a few GPIO from both the PI and the SMT32G4.  Why a 26-pin?  Other CAN tools I'm using also utilize this header and I didn't feel like making new harnesses.  Besides, it's a nice form factor for getting a lot of I/O and there are cables available on Amazon.

## Notes
This design is provided in KiCad 6.0

## Disclaimers
It has not been EMI or EMC tested.  I am not a hardware engineer so I can't ensure that there aren't some design flaws.  I've sanity tested the prototypes and they seem to be stable and perform as expected.

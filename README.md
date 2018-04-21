# myCRC

method of error detection for digital signals

why CRC ?
CRC vs parity ?

A parity bit check detects only single bit errors

CRC error correction allows detection of:
  1. single bit errors
  2. double bit errors
  3. bundled bit errors (bits next to each other)

Tx(Mtx) ------------------------------------------> Rx(Mrx)
if Mtx == Mrx No error transmission; else error in transmission.

Example:
Mtx = base2(110101) = base10(53)
let divisor = base10(5) = base2(101) = d
Mtx/d = 53/5 = 3 = base2(11)
Message with CRC = base2(110101) + base2(11) = base2(11010111) = base10(215)

mrx = 215

error check:
215/5 = 0 ==> No error



References
https://www.geeksforgeeks.org/error-detection-computer-networks/
http://ww1.microchip.com/downloads/en/AppNotes/00730a.pdf

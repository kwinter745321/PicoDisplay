# README.md Firmware

There are two distributions from Geoff Graham's web site:  PicoMite and WebMite.
PicoMite is for the legacy RPI Pico without the wireless.

## Required

Install TeraTerm.  The Pico will appear as a serial device running at 115200 baud 8-bit No parity.

## Terms

RPI     means Raspberry Pi
(cr)    Carriage Return.  You get this by pressing the Enter key.

## Deploy PicoMite

Connect a new RPI Pico board to a Windows Desktop, and a virtual drive will appear.
Drag the "uf2" file onto the drive.  It may be necessary to disconnect and reconnect
with the desktop.  Open TeraTerm, and connect to the recent new virtual COM Port.

You should be greeted with a prompt ">". Try entering: PRINT 2+2 (cr)
The deployment kit includes a User Guide.

## To Enter a program

! Here is what I do:

In the Serial Port "setup" in TeraTerm (with the baudrate), look for
Transmit delay.  I enter 5 msec/char and 20 msec/line. Then open the connection.

In the terminal, enter: NEW (cr) EDIT (cr)
Next use normal copy/paste in your desktop notepad/word.
Finally, use TeraTerm Edit function labeled Paste(CR) to paste into the EDIT terminal.
EDIT will receive the code.
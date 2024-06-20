# README.md - Demo

# TwoGaugeButton.txt

Firmware:  PicoMite 5.07
Devices: SSD1963 LCD Display (800*480 pixels)

TeraTerm Serial: 
BaudRate: 115200 8 bit no parity 1 stop bit
Transmit delay: 5 msec/char 20 msec/line

There are several ways to deploy a file to the Pico:
- Drag the file to a SD Card and insert the SD card into the display's SD Port.
- Inside a TeraTerm terminal session, enter EDIT mode and paste the code.

# Application explanation

The program demonstrates the GUI Controls and onboard device integration.  See Setup below.

The onboard device setup:
```
GP17 is connected to a onboard button.
GP26 is connected to the potentiometer.
Note: Analog is weird as GP26 is SETPIN 31.
```

On the display, press the "START" button. This action changes the state to "Running".

To show the Gauge controls, I set the first gauge value to 77.2.  The second gauge reads the values of the potentiometer only if the state is "Running".  Twist the knob on the potentiometer and the second gauge updates.  The second gauge color changes color to yellow when the value is above 40. It changes to red when the value is above 65.


# Setup

There is a one-time setup.  The values will be saved (but each entry causes the Pico to reset -- this is expected.  Just reconnect.)

For a five inch LCD Display, I use the following values.
These must be performed before loading/running the demo.
Each line must be entered one at a time and will reset the Pico.
(simply re-connect and enter the next line.)

```
OPTION SYSTEM SPI GP10,GP11,GP12
OPTION SYSTEM I2C GP8,GP9
OPTION LCDPANEL SSD1963_5, LANDSCAPE
OPTION GUI CONTROLS 75
OPTION TOUCH GP18,GP19
GUI CALIBRATE 1, 134, 3777, 2065, -1340
OPTION SDCARD GP22
```

Additionally, with an external RTC plugged into the PCB the date/time will be saved.  If there is no external device the app will set time at 0:00 and continue with local RTC time.

To set the RTC enter:
```
RTC SETTIME 2024,6,20,13,34,6
```

This action sets current date/time to 20 June 2024 13:35:06.

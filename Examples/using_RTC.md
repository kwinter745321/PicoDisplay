# using_RTC.md

Insert an external board with a DS3231 into the RTC port on the PCB.
Make sure to align the DS3231 with labels on the PCB.  No other wiring is needed.

Enter this command and then re-connect to the board.

```
OPTION SYSTEM I2C GP8,GP9
```

By the way:
The 32K and SQW pins are on a male header (in case you want to use them.)

You need to feed the RTC the current date/time:
```
RTC SETTIME 2024,6,24,15,08,34
```
Sets the RTC device to 24 June 2024 3:08:34

Thereafter, to set the clock in the Pico do this command:
```
RTC GETTIME
```

# I2C Connection explained

The OPTION statement sets the SDA/SCL pins for PicoMite.
The PicoMite has builtin an interface for various RTC devices.


# Getting a DS3231 external board


The board is inexpensive.  The example is two boards for $ 6 USD (24 June 2024).
Here is an example:

[Link to Amazon reseller](https://www.amazon.com/AT24C32-Replace-Arduino-Batteries-Included/dp/B07Q7NZTQS/ref=sr_1_3?crid=352NM68Y0F98C&dib=eyJ2IjoiMSJ9.Av0ZT44mgzkEZLgrGYpmsc1bvAskDxukuEiBsIwEXkbB7-zYm1yD3zXzsvQXjllb3Apxvfp1TCX6AwcA0wI3Y4wZtS34nBAqjnrT7VU5UvEfxpIw3OIQW18uLq0im_U5yxJ8Xk0C8MWByPLfO6GfQB7oVKYhrEsKwda6qcIWorG7Ipbgh2lcPhUxt8heLIHz-LtOZy4iwFEnVqmlKjJLoifrmVqpnKGpBPtLXY278Sg.ogIDrRRaQ6WGo77X34O05eURUW8gaICt-S_nZEiHdJc&dib_tag=se&keywords=ds3231&qid=1719256331&sprefix=ds3231%2Caps%2C224&sr=8-3&th=1)


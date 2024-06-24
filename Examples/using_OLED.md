# using_OLED.md

Some projects may need a simple display. An OLED is good for this
as it only uses the two I2C pins and power pins.  The PicoMite provides
a builtin interface for SSD1306 (the driver used by some inexpensive OLEDs).

Using this feature will require you to change the OPTION for the LCDPANEL which
means then only the OLED will display.  Also it has fewer features.

# SSD1306 Interface

The SSD1306 is using the same I2C interface as the RTC.
The reason it can do this is because I2C requires the program
to specific an address (which is usually unique.)
Enter these commands and then re-connect to the board (after each entry).

```
OPTION SYSTEM I2C GP8,GP9
OPTION LCDPANEL SSD1306I2C32, OR
```

The interface is discussed further at the bottom of page 46 in the PicoMite manuel and the drawing commands at the bottom of page 55.

# Getting an OLED

The board is inexpensive.  The example is one board for $ 7 USD (24 June 2024).
See the example below.  There are other sellers; one sells five (of the same) OLEDs for $15 USD.

[Amazon link](https://www.amazon.com/UCTRONICS-SSD1306-Self-Luminous-Display-Raspberry/dp/B072Q2X2LL/ref=sr_1_7?dib=eyJ2IjoiMSJ9.Av2lkLGBWPhH2qBAbn1mSPGKyQ_hVDqN0Om-UmYJrf66AKnS5ghnYLkISDHrowoVn3JVtTT_Uo-hErXM6t9OzJcPG2Qacl_p_UZH-B8G4lkxPxAXDiR8kLyEIffCPGqrLFmfqdZqydjQi-KF8i1q5_vDRzNBVLpCG8OV1FGXFY8Lymoi52qLgiCuzfjJp9IbrraFa7xp8nuWlPK8Ks0Ws3UTBIvT5c_tzrK99PAb4no.4Q8j3JX8r905cfQi57P-mMBIwlXPeo4LZ0CDPdsw_gg&dib_tag=se&keywords=SSD1306&qid=1711466280&sr=8-7)


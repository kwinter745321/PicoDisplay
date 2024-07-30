
# README.md - Examples

Simple examples to quickly learn the language.

# Examples
blink.txt
button.txt
read_voltage.txt
pico_touch_demo.txt



# blink.txt

Wiring Setup: The user connects a wire from pin GP21 to one of the onboard LEDs.

Using the onboard EDIT function, load the program text. Press the <F1> function key to save.
Then type 'run'.

The LED is lit and pauses briefly.  It then turns off the LED and pauses briefly.  
Then it repeats the above (until the user press Control 'c' in the Thonny shell pane.)


# button.txt

Wiring Setup: The user connects a wire from pin GP21 to one of the onboard LEDs.  Also, connect a wire from pin GP17 to one of the buttons.

Using the onboard EDIT function, load the program text. Press the <F1> function key to save.
Then type 'run'.

When the user presses the button, the LED is lit and prints a message to the Thonny Shell pane.  It then turns off the LED and pauses briefly. 
The program then waits for the user to press the button.  (To quit, the user can press Control 'c' in the Thonny shell pane.)

# read_voltage.txt

Wiring Setup: The user connects a wire from pin GP26 to the onboard potentiometer (device with the dial).  Also, connect a wire from pin GP17 to one of the buttons.

When the user presses the button, the ADC is read for pin GP26 and reads a voltage value since its connected to the 10K potentiometer.  It then prints the value. 
The program then waits for the user to press the button.  (To quit, the user can press Control 'c' in the Thonny shell pane.)

# pico_touch_demo.txt

Wiring Setup: No wiring required.

Scope
This program waits for the user to click the 'Start' button.  Then it allows the user to touch the area inside the Yellow Frame.  The coordinates
are then displayed in the HPOS and VPOS display boxes.  A third box diplays the merged XY values.  When finished the user clicks the 'Stop' button.

Since the Frame is on the right side of the display the coordinates subtract its Start X, Start Y value to display the 'relative' XY position to the user.


Using the onboard EDIT function, load the program text. Press the <F1> function key to save.
Then type 'run'.


![](/Images/Pico_Touch_demo.jpg)

# How to Load an Example


To enter an example in TeraTerm:

```
new
edit
```

This puts the user into EDIT mode.  Now copy the code from a notepad,
and paste it using the TeraTerm's paste key function (ALT + V) or
select it from the TeraTerm's Edit menu dropdown.

After pasting or typing the code.
```
Press the F1 key to save (and leave EDIT mode).

type RUN
```

This invokes the program. 

By the way, your code is saved within the Pico, so the next time you connect, the code is stil there.
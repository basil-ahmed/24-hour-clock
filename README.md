# 24-hour-clock
## VHDL | BASYS 2 Personal Project

### Code Snippets (in ISE):

![image](https://user-images.githubusercontent.com/90772853/223026683-50f74394-2ba5-4aaa-9f73-ff2a12a26d1c.png)

![image](https://user-images.githubusercontent.com/90772853/223026712-8f6e3df6-aaaf-4646-be54-d4e809bef462.png)

![image](https://user-images.githubusercontent.com/90772853/223026733-0221ab7b-370d-4c93-9347-de3c475ed992.png)

![image](https://user-images.githubusercontent.com/90772853/223026743-f3bdc92e-89a8-4ee1-9ac3-c5b4fc6c9e26.png)

![image](https://user-images.githubusercontent.com/90772853/223026762-8cedcf7e-31e5-45a7-aef2-3472fbb2d92e.png)

![image](https://user-images.githubusercontent.com/90772853/223026783-93b5dfb1-0e85-41b4-b541-2ad5ea29a7d8.png)

### Code:

This code is an implementation of a hex counter, which is a device that counts in hexadecimal (base 16). It is implemented on a digital logic board and consists of a 4-bit counter that increments its count on each clock cycle, and outputs its count to a 7-segment display to display the hexadecimal value. The counter is also connected to a set of LEDs that display the binary representation of the counter's value.

The code starts by defining the input and output ports of the hex counter. The clk input is a 1 Hz clock input, reset is a reset button input, and change is another input used to change the clock frequency. The leds output is a 6-bit signal that drives 4 LEDs, and the an output is a 4-bit signal that drives a multiplexed 7-segment display. The seg output is a 7-bit signal that drives the individual segments of the 7-segment display.

The code has two processes, the first process is a clock divider process which generates a 1 Hz clock pulse from the 50 MHz clock input, and the second process is a counter process which increments the counter and outputs its value to the LEDs and 7-segment display.

The clock divider process counts up to a certain number (50 million) before generating a 1 Hz clock pulse. It also contains a second counter, sec_counter, which counts the seconds elapsed since the counter started. If the change input is high, the clock frequency is set to a lower value of 250,000, and if the change input is low, the clock frequency is set back to its original value of 50 million. When the reset input is high, all the counters and variables are reset to their initial values.

The counter process increments the counter value by 1 on each rising edge of the clock input, and also updates the sec_counter variable to keep track of the seconds elapsed. It also has a counter1 variable that counts up to 4, which is used to select which digit of the 7-segment display is being updated.
The 7-segment display output process uses the counter1 variable to determine which digit of the 7-segment display to update, and then converts the value of the corresponding counter variable to hexadecimal and outputs it to the 7-segment display. The code uses four variables (hours, minutes, tens, and ones) to keep track of the time and display it on the 7-segment display. The tens and ones variables represent the tens and ones digits of the minutes, and the hours variable represents the hours. The thousands and hundreds variables are not used in this implementation.

### Labeled FPGA Board:

![image](https://user-images.githubusercontent.com/90772853/223026884-020b1008-1cd0-41f0-ad03-cfbf41ecfcc0.png)

### FPGA board pictures Reset Function:

![image](https://user-images.githubusercontent.com/90772853/223026953-694afaf1-46c8-480f-ac8b-06ea0cb9be13.png)

### FPGA board pictures 50Hz Clock and 200Hz Clock:

![image](https://user-images.githubusercontent.com/90772853/223027119-45c61dbb-9c21-463b-8792-ce10ce02f0ee.png)

![image](https://user-images.githubusercontent.com/90772853/223027124-dcfde444-b2c7-41fb-b06c-58061fb88b8c.png)

![image](https://user-images.githubusercontent.com/90772853/223027131-ab945c6b-5d61-4ab4-ae9c-c7d5ed2a36b7.png)

![image](https://user-images.githubusercontent.com/90772853/223027157-de32ac20-f5c3-4d23-8603-820ba2eb3834.png)

![image](https://user-images.githubusercontent.com/90772853/223027179-075c5eda-eaeb-4702-bbf1-de5b6aa00293.png)

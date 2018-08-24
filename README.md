Basys 3 General Input/Output Demo
==============

Introduction
--------------
This project is a VHDL demo using the Basys 3, switches, LEDs, pushbuttons, seven-segment display, VGA connector, USB HID Host port and USB UART bridge. When programmed onto the board, all sixteen of the user switches are tied to their corresponding LED. Every time a switch is toggled, the LED directly above it will toggle with it. The seven segment display counts up from 0 to 9 as long as no buttons are pressed. When BTNU is pressed, the first digit on the seven segment display is turned off. In the same manner, BTNL turns off the second digit, BTNR turns off the third, and BTND turns off the fourth. BTNC turns off the entire display and resets the counter. A computer monitor attached to the Basys 3 with a VGA cable displays a series of moving patterns. If a mouse is attached to the USB port, a cursor is displayed on the screen. For the USB UART, whenever the reset button or BTNC is pressed, the Basys3 will send the line “BASYS3 GPIO/UART DEMO!” to a connected serial terminal emulator. Whenever one of the D-pad buttons other than BTNC is pressed, the terminal emulator will print the line “Button press detected!”. For photos of this demo in operation, check out it’s page on the Digilent Wiki.
 
| Button | Function                                                          |
| ------ | ------------------------------------------------------------------|
| BTNC   | Turns off the entire seven-segment display and resets the counter |
|        | Prints "BASYS3 GPIO/UART DEMO!" through theUSB-UART bridge        |
| BTNU   | Turns off the first digit on seven-segment display                |                               
|        | Prints "Button press detected!" through the USB-UART bridge       |
| BTNL   |Turns off the second digit on seven-segment display                |
|        | Prints "Button press detected!" through theUSB-UART bridge        |
| BTNR   | Turns off the third digit on seven-segment display                |
|        | Prints "Button press detected!" through the USB-UART bridge       |
| BTND   | Turns off the forth digit on seven-segment display                |
|        | Prints "Button press detected!" through the USB-UART bridge       |
 
Requirements
--------------
* **Basys 3**:To purchase a Basys 3, see the [Digilent Store](https://store.digilentinc.com/basys-3-artix-7-fpga-trainer-board-recommended-for-introductory-users/)
* **Vivado 2018.2 Installation**:To learn how to get Vivado, see the [Installing Vivado and Digilent Board Files Tutorial](https://reference.digilentinc.com/vivado/installing-vivado/start).
* **Serial Terminal Emulator**: For more information see the [Installating and Using a Terminal Emulator Tutorial](https://reference.digilentinc.com/learn/programmable-logic/tutorials/tera-term).
* **MicroUSB Cable**
* **Monitor with a VGA port**
* **VGA cable**
* **USB mouse**
 
Demo Setup
--------------
1. Download and extract the most recent release ZIP archive from this repository's [Releases Page](https://github.com/Digilent/Basys-3-GPIO/releases).
2. Open the project in Vivado 2018.2 by double clicking on the included XPR file found at "\<archive extracted location\>/vivado_proj/Basys-3-GPIO.xpr".
3. In the *Flow Navigator* panel on the left side of the Vivado window, click **Open Hardware Manager**.
4. Plug a Basys 3 into the computer running Vivado using a MicroUSB cable.
5. Open a serial terminal emulator (such as TeraTerm) and connect it to the Basys 3's serial port, using a baud rate of 9600.
6. Click "Open target" in the green bar at the top of the window. Select "Auto connect" from the drop down menu.
7. Click "Program device" in the green bar at the top of the window. In the "Program Device" Wizard, enter "\<archive extracted location\>vivado_proj/Basys-3-GPIO.runs/impl_1/top.bit" into the "Bitstream file" field. Then click **Program**.
8. The demo will now be programmed onto the Basys 3. See the *Introduction* section of this README for a description of how this demo works.

Next Steps
--------------
This demo can be used as a basis for other projects, either by adding sources included in the demo's release to those projects, or by modifying the sources in the release project. Check out the Basys 3's [Resource Center](https://reference.digilentinc.com/reference/programmable-logic/basys-3/start?redirect=1) to find more documentation, demos, and tutorials.

Additional Notes
--------------
For more information on how this project is version controlled, refer to the [Digilent Vivado Scripts Repository](https://github.com/digilent/digilent-vivado-scripts)

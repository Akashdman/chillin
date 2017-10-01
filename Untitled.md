RASPBERRY PI CONNECTION
============

### FTDI BREAKOUT
1. Install FTDI Driver [here](http://www.ftdichip.com/Drivers/VCP/MacOSX/FTDIUSBSerialDriver_v2_3.dmg).
2. Connect the PiWedge to Raspberry Pi and FTDI Basic Breakout to its spot on the wedge.
>note: with the microchip facing up, plug the breakout in to the male header pins on the corner of the PiWedge
>note: Only use FTDI device of 3.3V or use 5V to 3.3V Logic Level Converter

3. Plug the Raspberry Pi power adapter into its port and connect the other end to an outlet.

Reference images:

![alt text](https://github.com/Akashdman/chillin/blob/master/ftdi-plugged.jpg "FTDI to Piwedge")

![alt text](https://github.com/Akashdman/chillin/blob/bf46ea57e36723021ec5ddc2282c1646cf1d2322/wedge-n-pi.jpeg "Pi Wedge to Raspberry pi")

***

### TERMINAL

#### Connecting via `screen`

1. Open a new terminal window and type the following command to connect to your Pi's console:
>Command line : `screen /dev/tty.usbserial[Press TAB to auto complete]`

2. Add the BAUD rate : `115200` and press enter.
>Command line : `screen /dev/tty.usbserial-AH02LSSH 115200`

3. Press `enter` to bring up the login screen.
> note : Once a connection is made you should notice that your terminal label will update to screen as opposed to bash.

4. Enter Login credentials.


#### Disconnecting via `screen`

1. Type `exit` and then hit `enter` to return to the login prompt.
2. Open a new terminal tab. `command+T`.
3. Enter `screen -ls` in the terminal and copy the Session number before .tty001 for use in the next step.
4. Issue the following command in the terminal: screen -X -S (session number) quit

***

### Troubleshooting

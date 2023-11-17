connect rpi to keyboard
read keystroke information 
transmit to lcd display



python inbuilt sys model used to gain access to standard input stream
when u execute a command, have 3 channels of information
	stdin
	stdout
	stderr 

system console is where you can recieve text and display information 
	there is usually a physically connected console with which to get the three I/O channels (for us, that is the connected keyboard)
usually, uses newlines to figure out when to stop looking for new information and to process the given string of keystrokes

alternatively, can use pygame module
	predefined functions for handling keyboard inputs
	pygame uses GUI


headless configuration - 
	allows u to control remotely using ssh
	i def want this as the base



i2c adapter reduces amount of pins from 16 to 4
	![[Screenshot 2023-10-14 at 6.54.44 PM.png]]
put header pins on breadboard
put pico (computer) on header pins, soder them all together


header pins - just connectors to the pins on the board. 


VIBUS pin (pin 40 on pi pico)
ground - ground pin on pi pico 
**Black is “GND” or ground.** **The red is “VBUS”, or +5 volts**.
sda pin goes to sda 0 (pin 1) on pi pico 
	a serial clock pin (SCL) that the Arduino Controller board pulses at a regular interval, and a **serial data pin** (SDA) over which data is sent between the two devices
	NEED SCL AND SDA FOR I2C TO WORK 
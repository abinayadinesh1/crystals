10/17
set up headless configuration with nils

## 10/18
had headless config set up, but something wrong bc cant run any commands on the rpi. reflash image, with same wifi setup, find port its running on, and try again. 

ping raspberrypi -4
1. take pictures with one camera
2. take pictures with 2 (how do i deal with not having enough pins)
	1. fuck me. not possible because:
	2. id need to buy a multicamera adapter, to have more input camera pins
	3. or id need a usb camera

# 10/19
figure out how to connect rpi to monitor and keyboard (so its not dependent on wifi)
	buy hdmi to micro hdmi connector!
power bank as supply - doesnt need laptop
found second webcam - need to synchronize picture taking in both

learned that you can use nano as a text editor on rpi!!!! 
set up rpi on small display, 

## 10/20
ordered e ink display
ideas:
	- in house typewriter station (can use for sandbox)
		- enter your name to start
			- (type in name, it generates a directory where the saved file will go, then opens a nano file for u to start typing with)
			- hit command x to save 
	- computer to use outside (so hard to work in the grass, glare on your screen, low battery power). biggest challenges are power and internet
		e ink reader, some sort of stand for it, on the back, attached is the rpi
		some easy established way to send pdfs/documents/files to it and then open them up and start typing
			no internet, focused laptop:
				read, write, build.
		simply:
			connect rpi to power
			find ip address using arp -a
			scp
	- lights controller
		- setting to change lights based on microphone or facial expression
	- desk buddy (lights, **weather** + time + date, calendar, open editor)
proper project is to 


script to take pictures every blank seconds
cron command
0 * * 10 * python3 /Users/abinayadinesh/Documents/scheduled_picture.py >/dev/null 2>&1
for once every hour, every day, of october


## 10/22
got e ink display, figured out how to set up hardware
impossible to ssh into my raspberry pi (hate)
FUCK YES. SO I CONNECT VIA DISPLAY, WAIT UNTIL IT CONNECTS TO WIFI, THEN FIND THE IP ADDRESS ITS ON. 
had to change my password



sensor fusion/multimodal learning for my project
	temperature
	soil moisture
	color of the soil 
		can write a script to take a picture every hour

want to work on typewriteerrrrrr but cant get my fucking display up and running
can wait until i get mouse






# ideas
1. camera set up on the gate to track how much foot traffic we have 

192.168.7.49

## spectroscopy with Scotch tape

### abstract

normal spectrometers have a one to one space to pixel mapping
	computational spec allows u to multiplex spectral data over a given sensor region
	from one unit of space on the sensor region, u will get one reading that turns into a pixel. we can turn this pixel of information into a 2d array of information? 
	multiplex - send multiple signals at the same time in the form of one signal. 


![[Pasted image 20230928124320.png]] normal computational spectrometer


DiffuserSpec is a simple computational spectrometer that uses the inherent spectral dispersion of commercially available diffusers to generate speckle patterns that are unique to each wavelength.

normal diffusers have spectral dispersion (diff frequencies of em waves get split from each other). take each separated wavelength and make a speckle pattern (imaged below) for it
![[Pasted image 20230928124534.png]]

### intro
normal spectrometers use an optical element, like a diffraction grater or prism to disoerse the broadband signal (aka a signal with a spread of frequencies) into its wavelength components. now, there is a one to one spectral to spatial sampling (for every wavelength we get a pixel whose value is the amplitude of the wavelenght). 

tradeoff between bandwidth (range of wavelengths u can get), dispersion angle (each color gets refracted at a different angle from the source which impacts us how? )

in an alternative setup, instead of getting one value being amplitude of that wavelenght, u get a spectrum. uses a spectral multiplexing element. these all use cool/expensive optical elements to do this. 

using scotch take as a dispersive element instead of a cool prism/fabricated material. then applying spectral multiplexing on the signal to get a spectrum per wavelength instead of a value of amplitude per wavelength. 

### diffuser spec outline
light passes through the dispersive element (scotch tape), a detector captures the amplitude? intensity at that point in space, map the input to the output speckle using a linear inversion reconstruction algorithm.
calibration step gives us the spatial-spectral transfer matrix (SSTM) WHICH IS THE SPECKLE PATTERNS FOR EACH WAVELENGTH. 
from this can we set up a system of lin equations to tell how much of each wavelenght came through? 

collimated light - parallelizes input broadband signal. 

CMOS (sCMOS) sensor - electronic chip that converts photons to electrons for digital processing


https://www.youtube.com/watch?v=FKJFIzDfUNE
CCD (charge coupled device)
	photosites - convert light to charge: charge is accumulated, trasnfered, then converted into a voltage and amplified then inputted to a analog/digital converter. 

matrix of vurrents are pased through a horixontal shift then a vertical shift to read the current at each value. 

analog - continuous 
digital -  [sampled](https://en.wikipedia.org/wiki/Sampling_(signal_processing) "Sampling (signal processing)") sequence of [quantized](https://en.wikipedia.org/wiki/Quantization_(signal_processing) "Quantization (signal processing)") values

CMOS (complementary metal oxide semiconductor)
	

both have millions of photosites (pixels). measure electrons ![[Screenshot 2023-09-28 at 1.29.50 PM.png]]


![[Screenshot 2023-09-28 at 1.31.29 PM.png]]

we have the sensor pixel measurements, by using calibration data we have th espatial-spectral transfer matrix (SSTM) WHICH IS THE SPECKLE PATTERNS FOR EACH WAVELENGTH. we want to find the intensity of each wavelenght, w. ![[Screenshot 2023-09-28 at 1.32.59 PM.png]]
define least squares and single value decomposition

To demonstrate the use of DiffuserSpec for spectroscopy, we first measured **A** for our ADE, Scotch tape, during a calibration step using a broadband superluminescent diode (SLD) source (Superlum, Broadlighter) connected to a custom-built monochromator with a spectral resolution of 0.1 nm

damnnn - broadband superluminescent diodes are super expensive and they made their own monochromator??!!

broadband superluminescent diodes

can use a fiber couple to direct light from a monochromator to two diff spectrometer setups

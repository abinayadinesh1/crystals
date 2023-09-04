[**Representing colors as three numbers (color graphics)**](https://ieeexplore.ieee.org/document/1463084)
- image encoded as RGB pixels --> rendered on device that can display RGB light
- CIE tristimulus values, XYZ = light intensity of the three primary colors
- models for color perception beyond tristimulus theory
- idea: the RGB values a digital camera reads is different from the rgb used to display pixels on a display. 

our vision is optimized for **electromagnetic radiation whos wavelength is in the visual spectrum** through the LMS cones/photopigments. 

spectral distribution = plots power as a function of wavelength
	in signal processing, will plot power as a function of frequency

trichromacy: all spectra, all spectrums, can be made up by  3 values
metamerism: 2 spectra that look the same can have different distributions? (more confusing)
	can make the same color in two diff ways. 
	two spectra are equal if they make indistinguishible trichromatic responses. 

computers that can display more than just RGB light? we can't immediately see it if its not on the visual spectrum
	[https://computergraphics.stackexchange.com/questions/10114/why-is-there-a-difference-between-the-cie-xyz-colour-gamut-vs-cie-rgb](A futuristic display device could be fed by images in XYZ space, for instance, and the device would decide how best to generate each color using the primaries it has available.)

perception of color: our cones process light in the visual spectrum through LMS cone cells
creation of color: 

convert spectra (RGB) to 3 cone response values (LMS) is like using a camera to make image pixels. how do you display these pixels?

<ins>color matching</ins>
lets build one. 
1. choose any three primary lights. (RYB) 
2. take a set of reference colors, ours are the monochromatic colors of the spectrum = single wavelength of light on the visual spectrum (same colors you get when you diffract white light.)
3. ask your observer to combine the original three primaries to get every color in your reference set. 

what is the point of the color matching experiment? 

tristimulus values must be made from a specific set of primary lights (RYB) and a specific observer (you). WE also have a specific reference set, monochromatic colors.

tristimulus values = once the match is made between the combination of primaries and some monochromat, a color can be defined by describing the amount of each primary needed to match it.

we have the tristimulus values for the visual spectrum now. 
**Tristimulus values =  the light intensity of the primary color values in a sample**

give everyone the same set of primary lights and they will use the same colors in the same amounts to make the tristimulus values. everybody will see the tristim vals the same. 

why would we care so much about color matching? based on some color, what do we think its made up of? if we wanted people to see some unknown color, how can we use what we know of how we perceive primaries and the target to make that color?

we need negative values in RGB for when, with only green and blue, our image is still too 'red' compared to the reference. 

****Tristimulus values =  the light intensity of the primary color values in a sample**** --> how much r, g, and b do you use? weights are from 0-255

to get the RBG values that represent a specific color, you need to know the weights of the tristimulus values. 
"To create the tristimulus values for an arbitrary spectrum, first multiply it by the color-matching functions, then integrate the result to get the total relative weights of the primaries, which are the tristimulus values for that color."
we have
- color matching functions = how to go from RYB to RGB
- tristimulus values = weighting that we experimentally figured out for the primary colors 
- tristimulus values for that color = weights of the primaries = weights of RGB ?  


### extra math
intensity :: (||electric field||)^2 +  (||(1/c)magnetic field ||)^2 = power transferred per unit area

power = dE/dt (change energy over time)
energy (Joules)

poynting = energy / unit area / unit time
integrate gives you total energy in a given region
irradiance

### questions
what are the color matching functions?
are the tristimulus values like the weights you need to apply to 
**Tristimulus values =  the light intensity of the primary color values in a sample**
RYB to get RBG.
RYB --> RGB
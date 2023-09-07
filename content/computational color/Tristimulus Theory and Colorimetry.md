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
all colors can be made by combining tristimulus values with primaries --> this makes a color matching function to encode something in RYB to RGB 

RYB + tristim values is a metamer to RGB. this is the foundation of colorimetry/color measurement. 

### CIE Standard Observer
CIE made some standard color matching functions that form a basis for coloromitry
one for 2degree fields (small) and 10degree fields (large)

![[Pasted image 20230904151958.png]]
CIE recommended color-matching functions (1931), also called the CIE 1931 standard observer. (Reprinted by permission from A K Peters Ltd.)

	Tristimulus values are vectors in a linear, 3D space defined by the primary lights. Transforming to a new set of primaries is simply a change of basis; it requires only the value of the new primaries with respect to the old ones. This is the link that ties XYZ to the physical RGB values of a computer display and is the foundation for all quantitative characterization of RGB color spaces.

### Transformations between RGB and XYZ![[Screenshot 2023-09-04 at 3.22.56 PM.png]]

kinda cool, RGB to XYZ preserves 3 dimensions, but XYZ for chromaticity gets rid of luminance (Y). CIE has brightness coded into the color space, as shown but the fact 
![[Pasted image 20230904152401.png]]

	All RGB spaces inevitably cut off a big chunk of the highly saturated green/blue colors.
	
	The XYZ space sort of has the opposite problem. All visible colors can be represented using only positive values in XYZ, but the XYZ primaries themselves are not physically possible colors—they're well outside the visible gamut.

you have an RGB characterization matrix to take you from RGB to XYZ. the inverse of that matrix takes you from XYZ to RGB.

![[Pasted image 20230904153304.png]]
heat a black body radiator to get a black body curve, white light lies near this curve. 

spectral locus = boundary of gamut = every point on the locus is a pure monochromatic light.
purple line = connects bound ends of the locus. every color on there is a combination of violet and red. 

### color vision
![[Screenshot 2023-09-04 at 3.37.27 PM.png]]
fire af

### nonlinear rgb
gamma functions = transfer functions
3d computer graphics is the only field where they keep linear mappings of rgb. 
display tech, digital video, and image encoding all map pixel values to nonlinear functions of intensity. 

now, transferring between color spaces is a little harder. transformation from RGB to XYZ requires the addition of three ID functions

	If the pixel-to-intensity functions are not scalar multiples of each other (which can easily occur in uncalibrated color systems, such as displays), then equal values of R,G, and B will not create a gray that is simply a darker value of white, but will have some tint depending on which primary is dominant in the blend.
VERY COOL. 

## closing
The cone response can be used to model adaptation, the way the cones adjust to changes in illumination.

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
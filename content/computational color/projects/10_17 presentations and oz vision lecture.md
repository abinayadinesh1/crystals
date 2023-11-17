## dichromat designers
people w more experise in drawing photoshops changes how comfortable they felt picking colors
drawing for themselves vs drawing for a trichromat audience

expert people usefd blend modes to achieve shading of the greens
what does it mean to have a hue score of 0?
1. adding text to colors on screen
2. switch the red channel with the alpha channel
people didnt pass ishihara test


used nix to find spectras of images
**printfab**, change color space of whats being printed
only using CMY, not K channel
	K = C + M + Y ? 
Neugebauer equations - what percentages of C, M, Y will add up to in the spectra
	INK gamut is smaller than tetrachroma
to find metamers, find points in the LQMS gamut that maps to LMS, just w diff Q
	diff Q stimulus, but similar LMS stimulus
using probabilistic models to model how many tetrachromats there were

## epsilon
infinigen intended for comp vis, allows u to procedurally make diverse 3d scenes. renders from noise using rules. rgb, occlusion normal depth maps. 
raster based render built into blender


## retinal sampling
coretsumo cone setup?
increase clumping factor = less leakage, more blurring at the edges. 
	WHATS THE OPTIMAL FACTOR

## nature vision
is a uv sensor even useful to measure wetness/dryness?
how do plant internals reflect UV? 350 nanometers



plants should be opaque in the UV spectrum, they are absorbed all the light at the 350 nm range
plants colored in epicuticular wax . 

the internals absorb uv at 350 nm
they end up reflecting a lot of UV bc of wax
reflectance of UV lowers as the plant gets yellower

epicuticular wax breaks down 


transmission peaking at 350. use light source to take image indoor or at night. 
disparity map shows the depth, shift from left image to right. really sensitive to parameter tuning. 
	align left to right
	align right to left
might need some advanced cross modal algorithm 
cant ignore disparity mapping at 
uv emitter as a floodlight to get better discrimination

## foursight
doesnt inc spectral locus but does make more of a distinction






optics, waves, signal processing, laura waller
neerja aggarwal - imaging and spectroscopy at the same time
try to teach finn things!



1_neural_scope.py
modify in this line
model.load_state_dict(torch.load(f'./model/{experiment_name}/{timestep}.pt', map_location=device))![[Screenshot 2023-10-17 at 2.41.08 PM.png]]


# hacking the human visual system - austin roorda
made first retinal mosaic!! 
background in physics, then optics of the eye, then structure and function of the retina
made AOSLP
image forming properties of the optics of the eye

control the stimulation of all the cones in the photosensor array
contraints and possibilities w this:
	LENS CANT FOCUS LIGHT INTO A FOCUS POINTS
	governmed by:
		size of spot = 1.22 (wavelength of input light stream) (focal length) / (pupil size)
		as aperture gets bigger, size of spot gets smaller. low wavelenght of light
		<mark style="background: #ABF7F7A6;">not spot, but gaussian blur. forms aerie pattern</mark>

	smallest point u can get is on the order of 2 arcmins/2 microns. 
	cones are on the order of 6 arcmins/5 microns. 
	foveal cones are smaller, peripheral cones are bigger. 

	optics of eye suck. laws of diffraction hold for small pupils, but 
		misshappen cornea, misalignment of cornea with lens. make image blurry as pupil gets larger. CAN RECOVER THIS BLUR. 
	collomated rays bc of the misshapen optics. 


measure the imperfections (integral to adaptive optics sensor) - WAVEFRONT SENSOR
	measure the properties of light that emerge from the eye. small spot of light on the retina, it scatters and u pass it through a 4f imaging system. lenselit array. measures the direction of all the beams emerging 

wavefront sensor: array of tiny lenses. take light coming out of eye, hitting array of tiny lenses
	if they were all going straightt, the wavefront would be flat and the CCD array would be sampled evenly. 
when wavefront distorted, ccd arra
**get distance between where the wavefront should be on the ccd sensor and where it is. get the slope, use to make the curve.**

achieve diffraction limited imaging. 
wavefront as a CONTOUR MAP. 

bounce it off a mirror with exactly the same shape, but half the amplitude. 



how do you shape a mirror?
<mark style="background: #FFF3A3A6;">defromable mirror tech - peizoelectric actuators. </mark>
	turbulence, temperature variance that causes the light to bend. why u cant focus light through the atmosphere. 
apply a voltage, can expand or attrach. 

electromagnetic actuators tethered to a membrane
go from large PSF to small, diffraction limited one

**how do we make a sharper image of the retina?**
deliver light to every single cone. 

have CCD camera just look at the retina

ao fundus camera, rochester

adaptive optics in a scanning imaging system. forms an image pixel by pixel by looking at the **scattered light from a focused spot**. 

confocal imaging system - allows u to record image of specific plane in depth (ours is the output of the photoreceptors)

### stimulus delivery
scanning imaging system
modulate the laser as it moves. 

big problem: human eye . moving target: how can u hit the target you want to hit?
where will the lazer be by the time it goes over the target
see where the retina is, arm the laser to deliver the stimulus

image w infrared. stimulate with green light. instead of turning off infrared, deliver microdose of green to that cone. 
	**blue focuses earlier than red.** when u deliver a flash, itll be out of focus and youll hit 20 cones instead of 1. 
		add a bit of negative power on the blue to push it back. precompensate scanning light for 
transverse chromatic aberration, and the fact they focus on differen places in the eye

polycarbonate flasses have a lot of chromatic dispersion
nobody measured transfers chromatic aberration

take 2 images of the retina w the diff wavelenghts, the lateral shift tells u chromatic aberration
obsessive about maintaining pupil position after correcting for chromatic aberration

every location in retina has diff chromatic aberration (CTA)
changes w pupil position

diff sensitivity if u hit the cone vs hitting space between the cone
	sensitivity threshold - 
	if ur targetting the gap, what are they seeing. what does the image show you? light is leaking arounnd the edges. 
	ADAPTIVE STAIRCASE
	hunt for the level where they 50% see. 

### remaining challenges
can target cones w visible light, image w infrared
ask the subject to question what color do they see when they stimulate individual cones. 
ren: what would happen if u only stimulated M cones
	was persistent and sent him a whitepaper outlining an experiment!
multiconjugate ao - astronomer have same problem when they try to look at big fields. 

oz vision : green experience - only activate m cones. 
HOW DO U KNOW WHICH CONE IS WHICH?
	org/volumetric methods to classify cone types. 
only display over as many cones as uve classified. nobody has mapped the distribution in the fovea. 

off axis aberration of the eye (eye is elliptic). visual system processes space and color differently. 

<mark style="background: #FFB86CA6;">visual neurosciecne talk: taking mri while driving</mark>
why scanning instead of holographic display (using SOM to deliver a whole pattern)
<mark style="background: #FFB8EBA6;">eye tracking embeddeed with imaging, same scanner can image and track</mark>

scanning might not work in a 10 degree field!!!!! only visit ur cone once - when u go through the scan . 

james fong

epm for apple vision pro display


consequences of looking at Oz
	things look so much better in Oz that you would be so sad without it

## ren- on photoreceptors

fundus view of the eye

disks are where the photopigments migrate and phototransduction happens

lot of amacrine cells that havent been classified yet
lateral inhibition circuit- reduces amt of power needed to convey message to the brain
encoded data stream about visual 



60nm

52mm filter
rgb one side, either ir or uv 
is there a light seal? 3d print a light seal 
	light control important to figure out
make a camera that shoots 2 pictures and align them
bit of cv used to align the two images - comp imaging piece to merge two images. do we want to remove the parallax

wide angle and shoot things farther away, parallax will be small
hack this to remove the board its tied to to tried to get the two cameras closer together. 

look at specs of camera module 3 
	hq: no lens, cmount lens. 
	plug into stereopi 2
	monoconversion - solvent thing
	sensitive to 250 nanometers
what wavelenghts matter. sub 300 nm, this setup wont work. lenses 
monochrome conversion

monochrome sensor (which we need from maxmax.com) goes down to 240 nm. emailing maxmax people and being like

do we want exactly the same unit or something a little different

off the shelf, in inventory, known supply chain
kolari vision, johnathon crowther who built some monochrometers to measure spectral response

the one we have rn does 350 
block visible ir
we need a filter that blocks out visible and ir, higher ir longer exposure (darker conditions)



project direction:
algorithm for finding the spectral responsivity of any camera (regardless/one parameter being the kinds of filters applied to it)
nvdi

deeper uv sensitivity (getting in the 220 nm range and high quality)
video?
imaging wo using the uv light source

### stretch goal!!!
**atmospheric photography** - 
heat in the sky
heat maps of uv/ir in the sky

uv filter


use a solvent to get rid of the chip (does he mean the color filter array) and then  
monochromatic camera - uv down to much lower light levels
if we want super good uv sensitivity, we would want to get the monochromatic camera from maxmax. 

uv/ir telescope


  

It **reduces the contrast between astronomical objects and the sky**, making some observations difficult, if not impossible.
do u always need a light source

image augmentation / super cool images w 5 channel data

how to mounting lenses on a raspberry pi hq 
light leaking (duct tape? 3d print a little mounter for it)


## what we have, current setup:
using raspbery picam 3
one camera in RGB (w ir cut filter)
noIR camera in RGB, UV, and IR (poorly in UV and IR, just from removing the IR cut filter)


alternatively use raspberry pi hq and/or monochrome camera (we could reach out to maxmax to get the camera they used for the research project)

### what do we want out of our camera setup?
stretch goal?
baseline image quality: image resolution (how many megapixels (12mp)), improve quality in deep uv (220 > )

monochrome camera - 240 nm, maybe more based on stereopi documentation


stereopi
1. mechanically fix how close the two cameras are (would be kinda easy)
2. build an algorithm that aligns two photos (easy)
opencv has homography for feature extraction/image alignment
	ir + uv harder to extract the features from bc theyre lower quality


ordered filters to remove rgb 
remove rgb and ir = uv
remove rgb and uv = ir

should we use a 3rd camera?
monochrome camera - stereo pi expeirment
rasppi3 noir + ir AND ADD monochrome camera

should we try to push for as low wavelength as possible

get RGB + IR working
first demonstration:
	**good camera images in RGB and IR** 
		adjusting for parallax
			making the cameras closer together
			having an image alignment algorithm
		adjusting for light leakage
		determining the range of light we are imaging: getting a spectral responsivity curves of the camera
			todo: design an experiment for this and get it checked by ren
		do we need an IR light source? will this mean if we need a UV source?

RGB + IR --> RGB + IR + UV
add a third camera with a filter on IR?  OR using 1 cam w rgb and 1 cam w UV + IR


RGB + UV and another RGB + IR
2 noIR cameras: 
	filters for IR and filters for UV
things we need:
2 noIR, 2 wide noIR
filter for UV, filter for IR




algebraically compute RGB given 

how do we get to this?
R+UV, G+UV, B+UV (1 camera)
R+IR, G+IR, B+IR (1 camera)--> need uv cut filter
	optimize for overlap between the two images (alignment)

train compneuro model w ok dataset and perfectly aligned one then very strong tetrachromacy should emerge

other setup would be one camera
IR + UV and other just RGB

IR + RGB + UV (without filters)
RGB (uv cut + ir cut filters)
-> (IR + RGB + UV) - RGB
assume blue: uv, red: ir

2 images

OR
1 camera dedicated to uv
1 camera dedicated to RGB + IR



calculate RGB from this


materials we need
third camera and ir + rgb filter (where we could look into a monochromatic camera)





experimental design
experimentally tell sensor quality --> what is the camera's sensitivity to what wavelenghts of light?
	split white light into its monochromatic elements. 
	apply a moving slit to get individual regions
	measure the intensity at each region (using what sort of device)
	measure camera intensity at that region and compare 


dependent on how much UV/IR enters the atmosphere





our dataset would be going into the compneuro model to see if tetrachromacy emerges
high performance image restoration from 2 images 
evaluation on comp neuro model

monochrome camera for UV - taking off the color filter array 
	monochrome doesnt get rgb, just UV
	black and white image (UV pass filter). 
	restoration for 3 cameras would mean a breakthrough

3 camera
	monochrome (1-\2 months)
	rgb
	rgb + ir
resotration algorithm for 3 image sources
syncing one button two two cameras 
do we have a practical path to this in the scope of the class?


### GOING FORWARD WITH 
**2 camera
	rgb + uv --> what is the sensitivity to UV here
	rgb + ir
algebraic image resotration
using filters otw (filter for ir, filter for uv)**



more sensitive to uv sensor --> ask maxmax ppl for their rphq setup? 
	boost exposure time 

getting spectral responsivity curves
image restoration
color mapping = how do we add these diff channels to get a really nice quality image
building a spectrometer/analzing gases from here
	microbes
feeding this into compneuro


filters on friday
cable by tomorrow? 






2 camera
	rgb 
	rgb + ir + uv (rgb filter to only get ir and uv --> ren)


rgb + ir
uv

(rgb + ir + uv) - rgb = 
image resotration:
	can be split up into homography, manual fitting, etc. 
	
kolari 850 and kolari uv
rgb cut filter?
[visible filter](https://maxmax.com/shopper/product/15131-xnitebp172-x-nite-band-pass-series-1-bp1-320nm-670nm-filter-in-72mm)

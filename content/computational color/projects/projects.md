
project backgrounds and mini lectures: what have we seen so far and what have we yet to see?

# A 
## project one: compneuro modelling 
this model is us trying to figure out how color distribution of a 2d image emerges from just an optic nerve signal. 

	decode the structure of the optic nerve signal, use that to get an image, then take the image and reencode it to build the nerve signal again.

  goal of this is to figure out if we can see what someone else is seeing just from their optic nerve signals. WHAT 2D IMAGE ARE THEY LOOKING AT, AT THAT POINT IN TIME. what is the color of this? 
	  this will help us model what its like to be colorblind. we can see what a colorblind person sees. 
	  can we also use this to see what a person with 4d color vision would see?
		  well, we have no way to display this in a way thats useful to us. 
		  can we use this to tell whether or not someone is a tetrachromat? yes, because the input will be very different from that of a 3d viewer.  
question: 
cda29 is a tartachromat. 
ishihara tetrachromat color test. 
	can have the wiring impossible to tetrachromats
	color image needs to appear somewhere. the neural correlate in the simulation is an image array, its a high dimensional pixels. 8 channels to make the color of a pixel. this is an upper limit. 
		gaps are not enough to makea whole nother dimension. neural circuity contrains. 
**optic nerve signals are encoding color for a 3d surface - what happens when we collapse this to 2d for the purposes of our modelling**
**what is the learnable function doing? what are each of the parameters encoding?**
what is 'percept' and is the translation just the perception at a future time step? percept is what we want the person to see
**do we have the response curves for a tetrachromat?** yes
**what does an optic nerve signal look like? is it like wavelength x intensity? what are teh dimensions/axis?**
**what is motion blur? does it have to do with saccadic movement? actually moving the eyes/head/object at a fast pace, or is it encoded in our cones?**

## minimal model of color vision emergence
taking the current compneuro model we have and trying to reduce the amount of learnable parameters and epochs we need to retain accuracy and still recreate the optic signal. 
question: can we explain the input and decoding function a bit?
![[Screenshot 2023-09-10 at 3.11.53 PM.png]]
## increase realism of eye simulations
open source matlab software package called ISETBio which enables you to generate spectral radiance scenes and then predict how the eye moves and what are the cone excitations (which cones are getting activated and where (cone mosaic)).

given a picture with RGB channels, (like a screenshot or normal image), convert this into a scene that seperates the image into many channels, each being a unique wavelength, where the image is light if that wavelength was represented and black if it wasnt. 
run these through some simulation of cone responsivity and use this to tell how we would see color in the original image. 

goals: 
given an original image (like from mac computer display), tell how our eyes would perceive the color in the original image. also, when we look at this image, which cones are getting excited and where?

**project directions**: try to encode temporal adaptation and blur within cone cells in the simulation. 
temporal adaptation? 
light adaptation: as there is more light in the visual field, the visual response also speeds up so we are more sensitive to fast moving stimuli. 


questions:
what is a spectral radiance field?
	radiance - radiation flux? how is that changing at a given point over time? well if it is at the same spot in space, shouldnt it be pretty constant? unless there are moving objects. 
how did they develop iset bio?
what are the parameters they are able to model and what makes them different from the biological processing of an image?
<mark style="background: #BBFABBA6;">how is temporal adaptation different from light adaptation? </mark>
<mark style="background: #BBFABBA6;">what is blur within cone cells?</mark>



# B
coretsumo - trying to boost human sight to 4D
retraining some of our cone cells to take a slightly different wavelength of information. mainly to perceive UV

### more context on oz vision
basically retraining some of our cone cells to process the same wavelenght of light differently. multiple percept from a single wavelength of light
its a new display placed on top of the eye that would enable u to see in more colors
wizard software layer built on top of adaptive optics scanning laser ophthalmoscope -AOSLO  correct high-order aberrations and provide real-time, microscopic views of the living human retina with unprecedented optical quality
### optimize experiments with coretsumo 
goal: how do we know that coretsumo works and users see UV?
question: what is a microdose?

## extending coretsumo to free gaze
currently we can only measure the cone response when the user is looking at a fixed point, 2 degrees away from the center (where light would hit their fovea). see if they can move their eyes freely and we can see how the mutant-IR cone cells respond. 

# C:
### Project 3: A Search for Human Tetrachromats
## make new tests for tetrachromacy
given jessica's geometry of 4D color vision, can we come up with tests for 4d. 
## others
1. get a printer to encode colors differently/better. are we giving it more/different basis with which to combine colors?
2. a projector for color display but with more colors. 
	1. what would this actually look like? 



# D
## build multispectral cameras / datasets
stereopi = captures stereoscopic images, which are just 2d images with an added depth. **this <mark style="background: #ADCCFFA6;">automatically captures RGB and UV</mark>?** dimension to make them look 3d

questions: **how do u modify a raspberry pi camera for deep uv sensitivity**
can use spectral filters for UV, visible and IR
CAN USE A SPECTRAL FILTER TO BLOCK ANY ARBITRARY WAVELENGHT OF LIGHT. MAYBE CAN ALSO DO IT FOR A RANGE OF WAVELENGTHS. 

FOR BUILDING DATASETS: why would a multispectral camera be better for getting the measured dimension. i was under the assumption that tetrachromats were seeing greater dimensions of light/impossible colors that still laid/were made up by wavelengths in the visual range. would a hyperspectral camera be a better proxy/data collector for this?

we have the retina mosaic (aka how are the diff kinds of rods and cones spaced apart) and are trying to predict what image the person sees dependent on this. so, how do we find the measured dimension and what is (<mark style="background: #ADCCFFA6;">confocal max flux</mark>)?
![[Screenshot 2023-09-10 at 6.47.45 PM.png]]

# e
## geometry of pentachromacy
analyze pentachromacy
	have u guys done anything with hummingbirds? seem like super hard subjects. no reason to believe their activity would be the same as a human pentachromat. 





design a camera
design a 3d projector
basic beam splitting experiments
BUILD A CAMERA THAT CAN MEASURE GAS FLUX. 
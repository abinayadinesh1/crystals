- What are the unknowns of greatest consequence in your pilot project plan, and are they potential showstoppers or potential gamechangers on the positive side? These almost always exist for a project.
unknown: how good the camera quality will be/how bad chromatic aberration is from the getgo

- What is the quickest / cheapest hack you can build / or investigation you can perform, to most clearly make the top unknowns a known quantity? I strongly recommend organizing your hackathon around these hacks and unknowns. Recognize that these unknowns and tasks often represent things that we know least well, and are therefore furthest from our comfort zone when starting a project in a new area.
how to build a camera --> build it 
    
- Converse to the previous bullet, what are things that you clearly know how to build or investigations you know the outcome of, that may be necessary to the project as you currently envision it, but will add less knowledge of consequence to the planning of your project? These always exist in projects. While they are critical to completion, I would write these tasks down and save them for later in your project -- it is likely that you will pivot your project in a way that makes some of these tasks irrelevant! Recognize that these points and tasks often represent things closest to our comfort zone, and it is often tempting to work on these first -- which is a project timeline mistake.
we clearly know how to:
1. collect data
2. analyze it 
application is less important until we have a really good camera built 

- What is something that you aim to build over the 4 weeks of your pilot project that clearly proves a hypothesis you have, and which will make clear your success and its importance (remember the little person on your shoulder asking: who cares?). This usually means building something unexpected and perhaps novel. For your mini-hackathon, identify the 3-5 major subcomponents of that something you will build. Define one of those subcomponents that you can build completely and demo successfully during mini-hackathon. Commit as a team to building it before you exit the room.
a mvp using stereoscopic cameras to build a camera that can take in information from uv, rgb, and ir. 
be able to look at the image quality from this rather than 
tell if we can use software post processing to take the data we have and actually use it to improve camera quality. 


a camera that can take in information/snap an image
https://stereopi.com/blog/deep-ultraviolet-imaging-using-raspberry-pi-hq-camera
Sony IMX477 sensor array happens to be pretty good in low wavelengths too

turn off the uv flashlight, turns into a monochrome camera. need uv light source
color DSLR modified for UV-VIS-IR
UV capable DSLR lens, like the Jenoptik 60mm APO costs $7,000 and the 105mm UV Nikkor copies cost over $8,000
For outside use, sunlight hitting the back of the HQ camera distorts the image.


goal: pentachromatic (5D) UV-VIS-NIR camera system
### making the camera ourselves
useful reference: people building uv camera out of raspberry pi hq camera
https://stereopi.com/blog/deep-ultraviolet-imaging-using-raspberry-pi-hq-camera
caveat: they needed their own UV light source, presumably we want to image UV light in front of us as it is? 

we have stereopi - two camera modules
raspberry pi cam module 3 - 
rgb - normal camera
ir sensitivity - using cameras with noIR filters
uv sensitivity -  the raspberry pi HQ camera sensor is pretty good at wavelenghts up to 240 nm- **how do we turn off  sensitivity to the visual range? to single out the uv**

take pictures in rgb, UV, and ir and layer them all together
1 image, not three images. 



design choice:
	3 images layered on top of each other or one image where we can separate the 5 channels?
	in the stereopi tutorial, they needed to shine a uv  light to be able to image uv at all in the image. do we need to incorporate a uv light source in ours as well?
	3 images in quick succession. click one button, stay in the same play and it will take three pictures that merge together into one in your gallery. 
	how will this image look? wht is the interface for navigating it?


### dual rgb imaging
https://www.researchgate.net/profile/Roy-Berns/publication/366441917_Theory_and_Practice_of_Dual--RGB_Imagingnm/links/63a1dd5cca6a9d254f8c9421/Theory-and-Practice-of-Dual--RGB-Imagingnm.pdf
rgb sensor w two color filters or two lights w diff color temperatures
pair of images (2 images) produces color managed rgb image and spectral image


**Crowther, Monochrome Camera Conversion: Effect on Sensitivity for Multispectral Imaging (Ultraviolet, Visible, and Infrared)**
https://www.mdpi.com/2313-433X/8/3/54#:~:text=With%20the%20monochrome%20conversions%2C%20sensitivity,compared%20to%20the%20monochrome%20conversions.
comparing sensitivities on normal cameras
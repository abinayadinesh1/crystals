## one

Current imaging systems, regardless of their color space dimensions, suffer from information loss due to convolution with specific frequency response curves. This results in a less-than-accurate representation of the original scene or object. Our ambitious goal is to deconvolve the projected measurement and thus reconstruct the full spectrum. Historically, hyperspectral imaging requires scanning-based element or low-efficiency filter array. [Recent work](https://opg.optica.org/optica/fulltext.cfm?uri=optica-2-11-933&id=332087) has utilized custom designed diffractive element to perform single-shot hyperspectral imaging. 

We plan to use off-the-shelf diffractive optical elements with known chromatic aberration properties. While chromatic aberration is often considered detrimental in imaging, we perceive it as a potential asset. Given sparse objects, especially in the microscopy context, or with prior training data for certain object types, we can exploit the spread of colors caused by severe chromatic aberration to assist in spectrum reconstruction. A spectrometer or sweeping laser might be required to calibrate the spectral response and validate our reconstructions. 

Our envisioned hyperspectral imaging system promises to be more cost-effective and user-friendly than current spectrometers, positioning it as a potential game-changer for capturing extensive full-spectrum data in diverse environments.


## two 
  
In the design of a UV-visible-IR camera, chromatic aberration poses a significant challenge, potentially leading to image blurring and a reduction in system resolution. This aberration arises due to the wavelength-dependent refractive index of optical materials, causing different wavelengths of light to bend at varying angles and focus at different points. In our specific case, where the wavelength range is broader than that of typical cameras, this issue is particularly pronounced.

  

Achromatic lenses, comprising multiple lens elements with distinct optical properties, collaborate to counteract chromatic aberration. Diffractive Optical Elements (DOEs) utilize diffraction patterns to manipulate light behavior, offering potential benefits in correcting chromatic aberration. Wavelength multiplexing imaging employs a collection of sensors, each sensitive to a different wavelength range. Chromatic aberration is subsequently corrected during image processing, resulting in accurate, aberration-free imagery. Spatial Light Modulators (SLMs) are versatile devices in optics and photonics. They offer dynamic control over various spatial properties of light, including amplitude, phase, and polarization. SLMs hold promise for dynamically correcting chromatic aberration in real-time. Leveraging extensive, high-quality datasets, neural networks have emerged as a powerful tool for reducing chromatic aberrations in images.

  

Our project faces two major challenges. First, the camera's broad wavelength range, especially in the UV spectrum, sets it apart from conventional cameras and requires specialized correction methods. Second, we aim to make this camera accessible in terms of cost, size, and usability. Our approach begins with a literature review to identify the best solution for our specific case. Subsequently, we will conduct simulations using tools such as Python, Zemax, or Comsol to optimize the design and validate its effectiveness.


### ren response  

Zahra, nice pitch!  I'd be glad to learn more about this project direction. Designing lenses is no joke, and generally too much for a class project -- depending on what you have in mind.  

I suspect that this [Dan Llewelyn's UV lens](https://maxmax.com/shopper/product/16030-m12-uv-6mm-f-2-8-m12-uv-camera-lens-6mm-f-2-8/category_pathway-2) is not well corrected for chromatic aberration (though I could be wrong). 

However, I'd be surprised if the Nikon or Jenoptik lenses were not very well corrected. 

- Nikon UV-105, 105mm f/4.5 Multispectral Imaging Lens 

- [http://www.company7.com/nikon/lens/0105f4.5uv.html](http://www.company7.com/nikon/lens/0105f4.5uv.html)

- Jenoptik UV-VIS-IR 60mm 1:4 APO Macro

- [https://www.photonics.com/Buyers_Guide/ProdSpec/Optics/UV-VIS-IR_60_mm_14_APO_Macro/psp6246](https://www.photonics.com/Buyers_Guide/ProdSpec/Optics/UV-VIS-IR_60_mm_14_APO_Macro/psp6246) 

  
  

diff wavelengths of light reflect differently, leading to chromatic aberration

if we want to expand cameras beyond the normal visible range, this might make chromatic aberration even stronger/the image quality worse

  

achromatic lenses counteract chromatic aberration

diffractive optical elements 

  

- cool team
- possibly building UV/IR/RGB camera
- looking at chromatic aberration for that camera

  
### three, aka compneuro
  
we know the s cone cells are widely sampled and often blurs the s component, but we dont know how this effects the actual image people are seeing and the blue component of it, because our gen neuro model isnt able to capture it. 


the emergence of color vision is super impacted by exactly where our diff types of cone cells are placed/how often they are sampled.  

gen neuro : optic nerve signals to reconstruct image  

the way we see things is quite stable, but if u look at our retinal images, they are changing super fast over time. 

our body is looking at things we cant see?!?!!??!!??!

  

fixational drift motion in the retina is good because it allows us to see properties of the world (objects, locations, ) while still having a stable image. 

  

extending anderson’s model (which uses bayesian inference to try to simulate how the brain learns whats around it)


1) to construct a biologically realistic cone mosaic **at the fovea**, and its corresponding RGC output

extending this beyong the fovea?

2) design a plausible set of stimuli to test the model

3) formally express the modified inference equations

  

1) test the limits of the model on color discrimination tasks

2) evaluate the of reconstructions. But really, my high-level goal is to provide a neural circuit model that’s exciting and productive for adaptive optics experiments and neurophysiology – and I would greatly appreciate suggestions on how to achieve that.

  

  

[https://www.sciencedirect.com/science/article/abs/pii/S1364661318301712](https://www.sciencedirect.com/science/article/abs/pii/S1364661318301712)

  

1. how spatial distribution of cone cells impact vision (at the fovea and beyond, the S cone configuration being very interesting here )
2. understanding contrast between stable percept for us and very unstable retinal images
  

3 project ideas:

build uv/ir/rgb camera

basic, could do myself if i wanted to

designing a lens to combat chromatic aberration is wide spectrum cameras!!

super cool, novel, goated team

  


## options
comp neuro ppl (much harder and less defined scope, should still reach out)

ashley (build camera)

zahra and ritwik, insanely cool, correct for chomatic aberration in hyperspectral imaging
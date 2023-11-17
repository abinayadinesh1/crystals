  

  

  

neuroscope: a way to look into a high dimensional percept and visualize it in rgb space

  

  

start with the optic nerve signal at time t: 

u have an rgb image

u translate that into lms activations: for each pixel, is it l, m, or s getting activated?

you represent that as activations in the cone mosaic

now u have a 2d image of cone activations  = optic nerve signal

  

percept is an image in K channels, which we can project into RGB space

  

  

after training, run neural scope.py

get the per

  

model —> result —? ns_fig —> model_3_tri_128

pred_ip_0_n where n goes from 0 to 10k steps

outputs the model’s understandnig of the image at certain time step intervals, 

  

  

model_3_tri_128

  

in main.py, if new_data_sample % 1000 == 0:

torch.save(model.state_dict())

  

  

train the full model

to visualize it, use comet_ml

batch trained

  

to evaluate it, run color matching

  

  

  

are we giving optic nerve signals to the model and why images?

NO

we GIVE natural images

we GENERATE optic nerve signals 

  

  

frm rgb image

retina model - ground truth retina cone mosaic (not a model, no training involved)

  

do spectral projection from rgb image onto retinal cone mosaic to get photoreceptor activations (this is what is treated as optic nerve signals)

  

neuroscope goes from k d percept to rgb image- so will tell u color dimensionality

  

run color matching function to get how much of each dimension it is

color matching error for each primary

finding minimum number of dimensions needed to match all spectral colors

  

error x dimensions

  

maxwell x grassman 

  

how many knowbs do u need to achieve the target color? 

  

the coefficients u get are a slice of the color matching function!!! thats soooo fraking cool. 

  

color matching function: 

at each wavelength from 400 to 700, how much of each primary color/activation of cone cell do you need to match the color? 

test this by looking at the perceptual difference between the color and the truthcolor mat

  

color matching functions - spectral sensitivity curves of three linear light detectors yielding the CIE tristimulus values X, Y and Z

  

  

our CMFS match stiles and burch 2 degree RGB CMF’s

MEAN SQUARED ERROR between our 

  

  

can change what model the color matching function is running with 

  

  

  

  

cortical model has 2 learnable modules 

neural bucket, to try to infer the cone identities in high dimensions 

cone identity function - have a pixel, want to identify which cone cell identifies to that pixel. 

  

  

how does the cone identity function work? you have a pixel (in rgb), and it identifies which cone cell will be activated based on that pixel. do we convert RGB to LMS coordinates and select the max of L, M, S to be the cone to represent that pixel? Then wouldn’t we be losing some information?

  

Or, does one pixel map to many cone cells (like if the 2d image was smaller than the cone mosaic), in which case we could add the activations of many neighboring cone cells to get the accurate value for the pixel?

  

PREDICTING WHAT THE BAYER MOSAIC IS

initially, we dont know anything about the distribution. 

  

  

  

learned cone identity function needs to be same as retinal 

  

  

**learned cone identity function is also k dimensional image**

retinal cone mosaic is ground truth

  

what would happen if you only gave yellow, blue dichromat imges

if u made it so l and m activations are always equal, the cone mosaic would not be inferred properly. 

  

modify each image in the dataset so whatever image u feed 

  

  

how to effectively generate dichromat data

  

  

6 mil images w/o gpu? 

  

has more complicated retinal model to play with

additional complexity
  
RGBA -> LMSQ
does maxmax have spectral sensitivity curves for those filters?
we need to get **lmsq**
spectral profile, take the points and save it as data

cone fundamentals
that is only spectral response function of the filter
pixel on the uv camera, value is 0.5, does that info along w the spectral profile of the sensor 


spectral profile of the filter and the pixel value, **spectral power distribution** 
0.5 comes from dot product of spectral power distribution of outside field and filter
integral of the intensities below 400 
knowing two of those of those doesnt give us the spd of the environment
- spectral power distribution of the outside field / environment
- spectral power distribution of filter
- intensity that camera registers

given that observation, its fair to start with rgb + ir as 4 cones

we have the spectral sensitivity of the ir filter, we have the intensity at every pixel, can we get the  spectral power distribution of the environment from that? 


what does the cone fundamental thing even mean for us?
dot product? 
we have a spd of the outdoor world and our cone lms has one peak
**ir filter has 1 peak below 400nm
define the ir filter as a 4th cone type**
	pixel value for uv is 4th cone activation


what is the cone fundamentals thing and why is it more realistic?

ideal case: if we had hyperspectral dataset with images as training data, we can define whatever cone fundamentals (the peaks for each cone) we want and take dot product to compute lms1 activations. 

<mark style="background: #FFB8EBA6;">take spd of outside environment from hyperspectral, define peaks for 4 cones, take dot product to get activation of each cone</mark>
![[Pasted image 20231114091619.png]]
collects hundreds of images at different wavelengths for the same spatial area


each image has hundred spectral channels, ranging from 400-700 nm
each pixel is a spectral power distribution
take dot product of each cone fundamental (lmsq) - move the peaks however we want - to compute each lmsq activation

pixel value of hyperspectral value (100d vector) dot cone fundamentals of one cone (100d vector)

  

we do not have a hyperspectral dataset
<mark style="background: #ABF7F7A6;">i would need spd of the outdoor scene to utilize our own cone fundamentals</mark>
<mark style="background: #FFF3A3A6;">impossible to predict spd of outside from the filter spd and pixel value. therefore, we’d still need to approximate outdoor spd. </mark>

  


we need to make specific decisions on what to model
nice if we could determine what species we want to model, because then we need to update retina model as well. 
currently, 3x3
num cones 3, assume human trichromat cone fundamentals
3x3 transformation matrix from rgb to lms

hummingbirds have 4 cone types, we dont know exactly how many there are 

  
change the peak of the q cone fundamentals 

didnt extensively study which cone peak works the best

but it peaking at 400 works, found using color matching functions

their dataset consists of hyperspectral images

  

  

open pickle file and see how data is being represented

if we wanna

  

  

tm- transformation matrix

they have from rgb to lmsq

i need transformation matrix to get us from rgba to lmsq 

  

transformation matrix is 3 by 4

  

  

rgba X tm = lmsq

  

rgb to lms 

  

rgb image - single pixel w 3 values: r, g, b

deifne the monitor we are gonna display the rgb image with : red, green, blue light, each with its own spectral power distribution (each with 100 dim vectors). weighted sum of eah of those w respect to rgb. 

rgb to spd for r, g, and b dot product w respect to lms cone fundamentals

element wise dot product between monitor spd and cone fundamentals - 

  

  

lms response = 

get transformation matrix by taking 

cone fundamentals * **spd for ‘display’**

  

**spd for ‘display’ - CRT monitor**

  

  

rgb + ir to lms q

rgb + ir triky

  

dont know spectral profile for ir light, come up w a 100 dim vector

define  

  

need cone fundamentals for q cone

  

cone fundamentals against monitor spd

  

need to modify retinal model




All of the colors we can see result from neural comparisons of all three retinal color cone types, and three primaries are necessary and sufficient to match any color


color vision =  stems from neural comparisons of all three, four, or more cone types, respectively


![[Pasted image 20231114110913.png]]
https://academic.oup.com/beheco/article/22/5/1042/252714#:~:text=A%20tetrahedral%20avian%20color%20space,tetrahedron%20is%20the%20achromatic%20point.

how are we evaluating this dataset?
we use Atsu's computational neuroscience model to try to **learn a retinal mosaic** from the images we provided. 
first, we feed in our dataset of natural images (scene)
then, these are transformed into optic nerve signals by being operated on by a fixed retinal cone mosaic (that we provide, and is standard across all training)
from original rgb values, we now have lms values for each pixel. these are the optic nerve signals that are inputted to the cortical model 

in advance, we decide to train the cortical model to learn 4 cone identity functions. 
the job of this model is to learn a cone identity functions for how many

cone identity functions are a NxNxK tensor

spectral identity of each cone (think of this as K-channel image)
The role of each parameters are simple - CIF (cone identity function) aims to learn the spectral identity of each cone (think of this as K-channel image) and injects those learned info into the input signal.

But as shown as Raw Color Embedding in the figure, each pixel is still missing in color. For example, consider a single cell (or a pixel). Even if we knew that the cell was L cone and label that corresponding pixel from optic nerve signals as L cone, it wouldn't change the fact that it is still missing M and S information. That is why we have our demosaicing network that interpolates the missing chromatic/spectral information from neighboring cells. You can think of this network as a simple CNN.




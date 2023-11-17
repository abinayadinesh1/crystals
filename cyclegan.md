how did mineral use cycle gan? to generate simulated images of different crops with pests/diseases/at varying conditions (maybe water/growth stage)

	In one experiment, Mineral [used a machine learning algorithm called CycleGAN](https://developers.arcgis.com/python/guide/how-cyclegan-works/), or cycle generative adversarial networks, to see if they could create simulated plant images of strawberries. CycleGAN generates realistic images, which Mineral can then use to diversify the rover’s image library. This way, when the rover encounters various scenarios out in the field, it can accurately identify specific crops, traits or ailments.


https://developers.arcgis.com/python/guide/how-cyclegan-works/

# intro to image to image translation models
arcgis supports Pix2Pix and CycleGan
![[Pasted image 20231115171012.png]]
satellite imagery to map translation

image to map
RGB to multi-spectral imagery
SAR to imagery
DSM to imagery
	digital surface models
	https://gisgeography.com/dem-dsm-dtm-differences/
	represents relief of a surface between elevation points
	https://www.lidar-america.com/digitalsurfacemodel#:~:text=A%20digital%20surface%20model%20
	generated from lidar data


main issue w pix to pix is you need a one to one relationship between satellite data and maps, or the pic ur starting with to the pix youre translating to. when your collecting data from different sources, this is not always garunteed. 

cycle gan is an approach to training a deep cnn for image to image translation!!
	using the deep cnn architecture, modifying it specifically for image to image translation


converting synthetic arperture radar data into rgb information
	what does SAR data look like?
	energy released from sensor, bounces back against the ground and 
		motion of the radar antenna over a target region to
	penetrates cloud cover
	emitting microwaves
	flood inundation, land cover changes, and modifications of the Earth's surface from landslides, earthquakes, and background tectonic motion

	NASA's Earth Science Data Systems (ESDS) program and Earth Observing System Data and Information System (EOSDIS) Distributed Active Archive Centers (DAACs)
		how to use SAR data from NASA
		https://www.youtube.com/watch?v=qlSXbrrR8dM
		https://www.youtube.com/watch?v=gcZL2-ixTiY
			ers 1 and ers 2 collect SAR data
		Combined Landsat and L-Band SAR Data: https://www.mdpi.com/2072-4292/10/2/306
convert rgb data to multispectral data
satellite imagery to map routes


# intro
cycle gan is built off of pix to pix
train two generator models at the same time and two discriminator models at the same time
can convert in the reverse direction
can use UNPAIRED DATASETS: wait what!!!!

# model architecture

![[Pasted image 20231116171900.png]]

first generator goes from image embedding of simple style map to transferred style map
second generator goes from image embedding of transferred style map to simple styled map
	probably u can update your loss to get closer to the original simple styled map

first discriminator learns the difference between the transferred style map and the original target map
	if we dont need paired images in cycle gan, how are we able to know the target image in the transferred style with which to compare our translation to?
second discriminator tells apart our reconstruction of the original simple styled map to the original


you know you're generator is good enough when the accuracy of your discriminator has gone up but now starts dropping again: it doesnt know how to differentiate the generated style transferred images from the targets. 


how does this work when you have unpaired images?


deep convolutional generative adversarial networks start with a cnn architecture? how does that work?




this is an adversarial process
[deep cgan tutorial from tensorflow](https://www.tensorflow.org/tutorials/generative/dcgan#:~:text=A%20generator%20(%22the%20artist%22,better%20at%20telling%20them%20apart.)

# How the loss is calculated while training?
for normal cnn's, last layer calculates the loss for every training example

#### loss for generators
1. apply adversarial loss! the generator tries to minimize the loss between it and the target, the discriminator tries to maximize the loss, find the most differences between the new style and the real image
	1. [[adversarial loss]]
	2. 
2. cycle consistency loss: make sure, in both directions, that after recreating the original map style from the transferred style, its as close as possible to the original. practice this in both directions. 
	1. it does this by calculating [[L1 loss]] (sum of the absolute differences between the expected and the predicted)
3. identity loss - trying to get the generator to keep the color from the input to the new style? 
	1. generator from domain a to domain a


[[cnn]]
[[gan]]

[[cycle gan code and more]]

### pix2pix

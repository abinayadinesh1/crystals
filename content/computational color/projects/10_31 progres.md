Distilling pose information from multiple angles to construct a 3D representation of a scene
	can be exported into unity, navigate through the scene edited using LERF, 

storyline
1. now that we can take multispectral images, we want to know how to maximize the information from them 
	1. recoloring into rgb so humans can see / get info from it
	2. 2d images to 3d via NERFS 
		1. how nerfs work (1 slide) 
			2. original paper: https://arxiv.org/abs/2003.08934 (Mildenhall et al.)
			3. tiny nerf: https://github.com/krrish94/nerf-pytorch (Krishna Murthy)
			4. blog post: https://dtransposed.github.io/blog/2022/08/06/NeRF/
		2. what can we try to improve? (1 slide)
			1. depth 
				1. https://barbararoessle.github.io/dense_depth_priors_nerf/
			2. multispectral nerfs 
				1. https://cvlab-unibo.github.io/xnerf-web/#
		3. why is this useful? (1 slide)
			4. gaming engines, robotics, urban design, transportation

evaluating multispectral images via the comp neuro model
1. naiive approach: just take a bunch of our images, train the model with it, and run the color matching function on the model to understand how many dimensions are needed to generate the colors in that image
2. in doing so, we ran into some important design questions:
		1. we have a big dataset of images the camera has taken: how many do we actually need to train the model? what is the smallest size/resolution we need to get proper color dimensionality? 
		2. to make this feasable, we have to be able to do it w limited compute (either on macpro cpu or on limited gpu's that atsu gave us <3):  we need to cut the image down into either 128 x 128 or 37 x 37 pixels
			1. downsample 
			2. patch
		3. what is the impact of misalignment of images on color dimensionality? 
		4. what is the minimal size we need 
		5. how big of a dataset do you need to get accurate images?

what is the 4th linear knob used by the color matching function?

slide 1
NeRF: Representing Scenes as Neural Radiance Fields for View Synthesis
![[Screenshot 2023-10-31 at 11.31.36 AM.png]]
H×W rays per pose.

P=vo​+t∗vd

original paper: https://arxiv.org/abs/2003.08934
tiny nerf: https://github.com/krrish94/nerf-pytorch

10:46-12 paper reviews
12-1 image processing and training
literature review
	intro to nerfs
		[Krishna Murthy](https://github.com/krrish94/nerf-pytorch) [`tinynerf`](https://github.com/krrish94/nerf-pytorch/blob/master/tiny_nerf.py)
	nerfs with depth?
	[cross spectral nerfs](https://cvlab-unibo.github.io/xnerf-web/)
	gaussian splatting
		structure frpm motion
		optimize 3d gaussians to represent the scene
		A600 gpu for real time rendering

rasterization - taking the image as a vector (shapes) and converting it into a raster image (a series of pixels, dots or lines, which, when displayed together, create the image)

multispectral nerfs
	why this matters
			better robotics - currently, even state of the art robots like SPOT only have access to builtin greyscale cameras. they use algorithms like Simultaneous Localization and Mapping (SLAM) to develop a 3d understanding of the world and their position in it. 
				being able to use our multispectral camera would open up a whole new world for what a robot can analyze about the world. 
					agriculture - crop quality, water, automated harvesting
				 would greatly benefit from having access to multispectral images
				with techniques like gaussian splatting (which )
multispectral nerfs for robotics 
Towards Open World NeRF-Based SLAM
https://arxiv.org/abs/2301.03102

oz vision training
image representation of multispectral images


**compneuro training**
good
2021-11-15_22-52-14.jpg.npy
2021-11-15_22-52-03.jpg.npy
2021-11-15_22-53-39.jpg.npy
2021-11-15_22-54-10.jpg.npy

bad
2021-11-15_22-53-34.jpg.npy
2021-11-15_22-53-52.jpg.npy
2021-11-15_22-54-03.jpg.npy
2021-11-15_22-55-18.jpg.npy
2021-11-15_22-55-20.jpg.npy
2021-11-15_22-55-22.jpg.npy
2021-11-15_22-55-25.jpg.npy
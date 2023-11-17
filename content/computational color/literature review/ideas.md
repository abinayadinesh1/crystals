have a 5 channel image

how do iphone solve for parallax w multiple cameras
	each camera has a different spectral sensitivity
	can tune each camera using filters to have the spectral sensitivities of specific animals
	can test how animals will see by changing 
	can we make a display to 

take a picture, where each lens has a diff sensitivity
the picture is all layered on top of each other
going through each of the channels of our picture should allow us to see what a hummingbird finds important vs what we find important




cheap phones
e ink readers
	display takes no energy when you are just reading on the screen, only takes energy when you need to change what is on the display
		how do u scroll
		how fast is the process of sending electrical charge and changing which particles come up?
	https://www.howtogeek.com/752328/what-is-e-ink/

![[Pasted image 20231010140831.png]]
https://spectrum.ieee.org/how-e-ink-developed-full-color-epaper


used uv lightsource at 400nm
put leaves in dark chamber, add uv light source, measure uv reflectance
looking at bird foraging behaviour
dark berries are hidden in bushes, but the black surface of the berry might actually reflect a lot of uv which hummingbirds can see


ultraviolet reflection of berries attracts foraging birds
mouse s cone is also sensitive to UV
contrast from uv enables them to see predators?

UV green image that mimics mouse vision?

sceneCam for recording mouse movies


how to align diff images:
	cross modality registration framework:
		feature extraction
		feature matching
		transformation estimation to get features to match (translation, rotation, scaling and deformation)
pia fusion algorithm 

cycle gan making pseudo ir image to original image
	need better model tho
	visible and ingrared uav target image registration
	gan to generate other image based on visual image
	structure correction network to make pseudo ir image
	pseudo ir and ir fed into second part  and we find the coefficient between both. 
	do optimization of alignment based on error. 
general cross modality registration framework for uav vis and ir


plants see infrared more than anyti=hing else
trees are red because of false color representation
	in rgb we actually collect 7 bands of information


stereoscopy
alignment on drones/satellites are a lot harder
how can we get from a pair of 2d images to 3d information?

stereoscopy - use a pair of 2d images to get 3d information
originally designed to make a depth map of the scene
	very cool if we could make nerfs from this??
just change one of them to be a diff spectral range
**multi spectral stereoscopy**
	set of mirrors and filters to make diff color channels
	each camera is at a diff angle because 
disparity map enables 3d surface reconstruction
longer wavelengths can penetrate the celery and give u more deep 

cross spectral stereo matching
gat between 2 spectral bands

multispectral but might also give u stereo infromation of the scene
1. image registration --> multispectral imaging
2. cross spectral stereo matching --> scene depth match
3. multi dim datasets to train network for better plant characterization 


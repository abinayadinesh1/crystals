### 1

background: goal of computational neuroscience model is to figure out if we can <mark style="background: #D2B3FFA6;">see what someone else is seeing</mark> just from their <mark style="background: #D2B3FFA6;">optic nerve signals</mark>.
**use cases:** <mark style="background: #FF5582A6;">needs strengthening</mark>
	model what its like to be color blind
	use this to tell who is a tetrachromat and who isnt (will the incoming signals be much different?)
	use this to see what a tetrachromat sees (how would we display that extra dimension?)

being able to reduce the parameters necessary and epochs we need to train for will be a useful ml experiment.

### 1.5
increase realism of isetBio
does isetBio take the scene and then show us how the brain/we encode the scene? can we construct a scene that is different from what the user would see? 

	what is isetBio trained on?

so far it can tell us: 
	- how the eye will move (how it will take in the image? what it will focus on first? this is a static scene, so are we trying to understand what area the brain will focus to first?)
	- which cones are getting activated and where?
<mark style="background: #FFB8EBA6;">	- how are our eyes perceiving color
</mark> related to question about how this is different from the compneuro model


	"what visual stimuli captures our aattention/focus the most" is a very interesting question for user experience/interfacing

	
possible research directions:
1. use this to see how a tetrachromat percieves input stimuli. run our simulation on a image only a tetrachromat would be able to get useful information from and see how the simulation performs. 
2. encode temporal adaptation
	1. light adaptation - more light, faster response, more fine sampling. 
	2. what would it look like to build on top of isetBio? what frameworks/stacks/languages would you be using?
<mark style="background: #FF5582A6;">3. encode cone blur</mark>

# 2
use cases of mspi
- train a model to tell when a plant is stressed
- use this to calculate how much water is in a plant stem
	- infrared cameras are used to measure **plant and leaf temperature** in a non-destructive manner, which is **indicative of plant water use** behavior, including transpiration and leaf stomatal conductance
use cases of hspi
- construction: what part of ur wood is damaged by moisture
- detect impurities in rice
- be able to see more differences in color than not
	- train roombas to detect dust on the floor better
	- **The infrared sensor at the very front of the Roomba allows the vacuum to bounce light off an object to detect its presence**. BRUH dust doesnt emit heat, why are we using IR!!!?
can make uv, ir, and visible camera!!

[stereo pi readings](https://stereopi.com/blog/deep-ultraviolet-imaging-using-raspberry-pi-hq-camera)
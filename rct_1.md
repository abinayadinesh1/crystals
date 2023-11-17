
blog: https://blog.research.google/2022/12/rt-1-robotics-transformer-for-real.html
paper: https://arxiv.org/abs/2212.06817

normal ml is able to combine diverse datasets with architectures that are able to pick up and use all this nuance
robotics is really one step behind
	previous attempt was trying to broaded the kind of data that the robot trained on to be able to generalize to novel tasks better
		the robot learned from demonstrations, interventions (?), and was conditioned (?) by different forms of information like pre trained embeddings of natural language (damn is this multimodal? having these embeddings in the same space as the visual demonstrations?) and videos of humans performing the task
	used large-scale VR-teleoperated dataset of demonstrations for 100 manipulation tasks, and train a convolutional neural network to imitate closed-loop actions from RGB pixel observations
biggest problem is the lack of large scale diverse data:
	every lab makes their own task specific demonstrations to train their robots, then dont share them for public use. 
		chelsea finn initiative to combine datasets for general training
	dataset curation requires autonomous operation
		<mark style="background: #ABF7F7A6;">autonomous</mark> - be able to generalize to new tasks
			https://karolhausman.github.io/mt-opt/
			large-scale collective robotic learning system can acquire a repertoire of behaviors simultaneously, sharing exploration, experience, and representations across tasks
			getting multiple robots at the same time to perform different tasks and for them to all learn from one another
				why cant robots from other labs also share experience from these?
		<mark style="background: #ABF7F7A6;">operation</mark> - be able to handle diff kinds of objects
			how do we get robots to be able to work with many different kinds of objects?
			**RGB-Stacking as a new benchmark for vision-based robotic**
				combination of simulation and real-world data to learn multi object manipulation
					[their simulated environment](https://github.com/google-deepmind/rgb_stacking)
<mark style="background: #ABF7F7A6;">		lack of expressive, scalable, and fast-enough-for-real-time-inference models</mark> - being able to learn from data, cutting down inference time

## robotics transformer 1!!
trained on multi tasks
can tokenize a bunch of shit together so its easier to do real time inference:
	in the same embedding space, have camera images, task instructions, and motor commands
		camera images: rgb + d (?)
		task instructions:![[Screenshot 2023-11-12 at 3.38.54 PM.png]]
		motor commands:
			%% Command:
			- Motor 1: Rotate clockwise at 50% power
			- Motor 2: Rotate counterclockwise at 50% power %%

fucking hell they had to train all their own robots:
	made a robotics dataset of 130k "episodes" that cover 700+ tasks, collected using a fleet of 13 robots from [Everyday Robots](https://everydayrobots.com/) (EDR) over 17 months
this model can do 
	zero-shot generalization to new tasks + new environments
the rt1 transformer:
	inputs: snapshots from the robots camera and task descriptions in natural language
		need to read clip on how this is put in the same embedding space
	outputs: tokens for the actions the robot needs to take
how did they build the architecture? its modelled after a decoder only sequence model trained against standard categorical cross entropy objective with causal masking
	wtf does this mean:
	[[basic nn, how does one learn?]] 
		decoder only sequence model:
[		standard categorical cross entropy objective:](https://en.wikipedia.org/wiki/Cross-entropy#Cross-entropy_loss_function_and_logistic_regression)
			deep
		causal masking: 
features of the architecture:
	image tokenization:
	action tokenization:
	token compression: picking the tokens most important for the task so inference time can get faster
		

### dictionary
closed-loop actions - sensing, processing, decision making, taking actions, getting feedback
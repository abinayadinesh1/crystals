sim 2 real - 
	simulation is less expensive
	less dangerous
	ex: open ai's rubiks cube
		con: does not generalize to the real world
		overly simplified model makes it harder to generalize

simeon doing - deep-learning computer vision-based human-following robot for elderly fall detection


ROS:
	broadcaster
	listener
	frame
	

- [MeshRender](https://github.com/BerkeleyAutomation/meshrender) - A set of Python utilities for rendering 3D meshes with OpenGL
- [Perception](https://github.com/BerkeleyAutomation/perception) - AUTOLab’s toolkit for robot perception tasks
	- documentation https://berkeleyautomation.github.io/perception/
	- library made to help implement robot perception
		- enteroreceptive sensors, that sense things inside the robot (e.g. joint angle,speed, torque) and
		- exteroreceptive sensors, that sense things outside the robot (e.g. proximity, vision).
- - [RAPID](http://rapid.berkeley.edu/) - Robot-Assisted Precision Irrigation Delivery (RAPID) is a co-robotic approach where a team of humans and robots move through the fields to adjust low-cost adjustable drip irrigation emitters at the plant levels
	- what is the cost of this system? who would have access to it? 
	- what irrigation systems is it compatible with?
	- how much human involvement is necessary?
	- how much money do u save from doing this? 
	- what if u dont have the water (insane drought in central and sacramento valley 
	- https://www.latimes.com/environment/story/2022-11-23/drought-cost-california-agriculture-1-7-billion-this-year)
		- 20% of land in fallow
		- Multi-Robot Routing Algorithms for Robots Operating in Vineyards
	- what kinds of crops
	- further development in robot perception? 
		- how are you guys measuring water content? 
		- what else could we measure that would be useful? 
		- pod counts, leaf area, flower counts, petiole lengths, fruit defects and disease
Alpha Garden
	coverage, diversity, water usage
	staggered planting for slow growing plants to not get outcompeted
	alphagardensim
		irrigation, pruning, planning
		overhand cam to feed in priors
	
  ![[Screenshot 2023-10-30 at 4.24.04 PM.png]]
![[Screenshot 2023-10-30 at 4.23.52 PM.png]]
	gantry robot
	solenoid valve
	
](https://autolab.berkeley.edu/)



Evo-NeRF: Evolving NeRF for Sequential Robot Grasping of Transparent Objects.](https://www.google.com/url?q=https://drive.google.com/file/d/1N1DYczxpgIRRKDZse4DSXX9n_42UiuAX/view&sa=D&source=editors&ust=1698711446925860&usg=AOvVaw2wZ3dKYdEnwgmNVZ8TaQhP)  Justin Kerr, Letian Fu, Huang Huang, Jeffrey Ichnowski, Matthew Tancik, Yahav Avigal, Angjoo Kanazawa, Ken Goldberg.  Conference on Robot Learning (CoRL), Auckland, NZ.  Dec 2022. [[Paper]](https://www.google.com/url?q=https://drive.google.com/file/d/1N1DYczxpgIRRKDZse4DSXX9n_42UiuAX/view?usp%3Dsharing&sa=D&source=editors&ust=1698711446925984&usg=AOvVaw1DvLdPwryv0rRbLGTXIgrZ)
	evo nerf
- Evo-NeRF terminates training early when a sufficient task confidence is achieved
- evolves the NeRF weights from grasp to grasp to rapidly adapt to object removal
- applies additional geometry regularizations to make the reconstruction smoother and faster
- Radiance-Adjusted Grasp Network (RAG-Net), uses depth as well
- Instant-NGP - a faster version of nerfs
- by re-using NeRF weights from grasp
to grasp and demonstrate its rapid adaptability to object removal


Since we propose that the robot captures images and trains a NeRF as it moves, motion blur, kinematic limitations, and speed considerations reduce the quality of the recovered geometry and introduce prominent spurious geometry known as floaters. We propose adding geometry regularization to the training objective, which improves the recovered geometry, but out-of-the-box grasp planners still struggle to find quality grasps due to remaining artifacts.



[Fleet-DAgger: Interactive Robot Fleet Learning with Scalable Human Supervision.](https://www.google.com/url?q=https://arxiv.org/abs/2206.14349&sa=D&source=editors&ust=1698711446926296&usg=AOvVaw0XHk0ThoBJWg2td_4tdhmp) Ryan Hoque, Lawrence Yunliang Chen, Satvik Sharma, Karthik Dharmarajan, Brijen Thananjeyan, Pieter Abbeel, Ken Goldberg. Conference on Robot Learning (CoRL), Auckland, NZ.  Dec 2022. [[Paper]](https://www.google.com/url?q=https://arxiv.org/abs/2206.14349&sa=D&source=editors&ust=1698711446926415&usg=AOvVaw2XQpJnUIAnXOxQXfFLv8lE)
	fleet dagger
	
[DayDreamer: World Models for Physical Robot Learning.](https://www.google.com/url?q=https://drive.google.com/file/d/18FA4F4cw53rWXLwvAKN4GLTpBT8RFM9q/view?usp%3Dsharing&sa=D&source=editors&ust=1698711446926760&usg=AOvVaw3Oy4nnpZBGBTB9OFGttIbn) Philipp Wu, Alejandro Escontrela, Danijar Hafner, Pieter Abbeel, Ken Goldberg. Conference on Robot Learning (CoRL), Auckland, NZ.  Dec 2022. [[Paper]](https://www.google.com/url?q=https://drive.google.com/file/d/18FA4F4cw53rWXLwvAKN4GLTpBT8RFM9q/view?usp%3Dsharing&sa=D&source=editors&ust=1698711446926933&usg=AOvVaw20JOY2YfchW-VXwyjb_Yd8)

[All You Need is LUV: Unsupervised Collection of Labeled Images Using UV-Fluorescent Markings](https://www.google.com/url?q=https://drive.google.com/file/d/1XQofTiAC5uXqjAaMUZcBTWTYE2b-LprL/view?usp%3Dsharing&sa=D&source=editors&ust=1698711446927676&usg=AOvVaw39-xGTUMNUWIFK1XejYGBv): Brijen Thananjeyan, Justin Kerr, Huang Huang, Joseph E. Gonzalez, Ken Goldberg. IEEE/RSJ Int’l Conference on Robots and Systems (IROS), Kyoto, Japan, October, 2022. [Presentation Video](https://www.google.com/url?q=https://drive.google.com/file/d/1bscfdmAG5TXZzGTFMiSfrNa3FY_YkNEg/view?usp%3Dsharing&sa=D&source=editors&ust=1698711446927780&usg=AOvVaw3DMOeO7m19JbEIhSOesC9r).
	take normal rgb image
	color w uv paint, take another image
		WHO IS COLORING IT - WHO IS LABELLING IT?
	the uv paint is like a labeled 

[[lab_meeting_10_30]]
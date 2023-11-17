corl coming up
contextual learning - prompt structuring
HANDLOOM - cable tracing

**next on alpha garden**
	nerfs so we can get height
	better growth models
	
can we do Unsupervised Collection of Labeled Images with a multispectral imaging system? 
Evo-NeRF: Evolving NeRF for Sequential Robot Grasping of Transparent Objects
fleet modelling

topological data analysis
	deformable object's local geometry constantly changing
	global structure: connectivity, obstruction to connectivity
2 ways to analyze:
persistent homology
mapper algorithm
	take input point cloud
	lense function f that operates on point cloud
	each node is a collection of points from the original point cloud
	finding connectivity from nodes (based on overlap of bins)

UMAP - uniform manifold approximation and projection for dimension reduction
	its a lense function for the mapper algo
	takes the original point cloud and INFLATES it to exaggerate structure
	good sampling complexity - less nodes for same amt of sample points 
	very low dimensionality, less samplings, but getting lots of detail



deformables: 
	objects that bend and fold. if we keep running mapper on it, we keep getting diff outcomes.
	get sequence of point clouds over time
	match outputs between time steps to get structure
	use output at t-1 to get output at time t

mapping onto r3 space
dgcnn doesnt work well on deformable objects
sim dataset of labelled trajectories using meshes from DEDO
	how to lable components of the SIM as it deforms through time


surgery
hansoul 
applying **homogrophies** to pcd to move to correct overhead 
wound id - sam edge detection



notes to take away
need to learn about nerfs, people who have tried to do multispectral ones, adding depth to nerfs
what is a homography?
checkerboard calibration matrix for aligning our images?





stereopsis gives point cloud from left and right images
needle pointcloud
ransac algo to predict 

get pointcloud of front, top and side views
get a lot of depth artifacts that make it super hard to do ransac
	Randsac circle fitting makes a taurus. depth artifacts get too involved. 
	used open3d to publish images, matplotlib is better. 
raft stereo 
image alignment of masks on stereoscopic cameras

fastraft point clouds dont have straight line artifacts
perspective and point - how to get camera angle from images



using gaussian blur to reduce reflectance of the material
kalman filter

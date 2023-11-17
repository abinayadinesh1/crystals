hugeee explanation of all the arithmetic
https://arxiv.org/pdf/1603.07285.pdf

slightly shorter explanation
https://arxiv.org/pdf/1511.08458.pdf
<mark style="background: #FFB8EBA6;">fully read!!</mark>


input: multidimensional vector
input --> input layer --> hidden layers --> output classes
hidden layers: make decisions from the previous layer, and weigh up how small, random changes to its internal structure changes the output (learning)

![[Screenshot 2023-11-15 at 5.31.29 PM.png]]

this is how a feedforward neural network, restricted boltzman machine,and recurrent neural network is strcutured

supervised learning - attempting to minimize classification error
	bro most image processing still leans heavily on having labeled datasets
unsupervised learning - reducing some sort of **cost function**  (applied to the average of the loss function values over all the samples)

## intro to cnn
neuron - takes input and multiplies it by some scalar then does a non linear function (like a polynomial)

the last layer is where u have a loss function for each of the classes (applied with every training example)


cnn's are mainly for pattern recognition within images, allowing us to encode specific features we are looking for in the architecture


MNIST dataset
	28x28 pixels
	handwritten datasets and their labels

	one neuron has 28x28x1 weights, a weight for every pixel and every channel. 
	what is weight? how important that pixel is ?

for bigger images and more color channels, why cant u just increase the amount of layers and neurons in each layer?
	1. not unlimited computational power + time
	2. dont wanna overfit to this dataset

each neuron in a cnn has three dimensions, height, width, and depth (3rd dimension of an activation volume)

not fully connected/densely connected

input dimensions are 64x64x3, output dimensions are 1x1xn
![[Screenshot 2023-11-15 at 5.43.52 PM.png]]

input layer - pixel values of the image (height x width x n)

has 3 types of layers:
### convolutional layers - 
- neurons are connected to local regions of the input
- determines the outputs of neurons by taking the scalar product between its weight and the region connected to the input
- RELU applies a neuron wise activation function on the outputs of each layer, tries to prevent vanishing gradient/local mini
this layer depends on learnable kernels
when data hits a convolutional layer, the layer convolves the input across space (via the kernel) and makes a <mark style="background: #ADCCFFA6;">2d activation map</mark>

trying to learn kernels that fire when they see a specific feature in the input vector
		every kernel has its on activation map, or feature map. 
		kernel - looking for specific features?  if it finds it, it will have a high activation map, the feature was found
		filter = kernel
			**designed to detect specific patterns or features in the input data**.
		activation map = feature map
		
![[Screenshot 2023-11-15 at 5.56.59 PM.png]]
receptive field size - how much of the input image is the neuron connected to?
![[Screenshot 2023-11-15 at 5.59.58 PM.png]]

### hyperparameters that optimize the output and reduce complexity!
depth - how big is the output volume produced by the conv layer?
		how many neurons in the layer connect to the same region in the input?
stride
	how often do we set the depth around the spatial dimensionality? how much overlapping do you want of the images to the input?
	
zero-padding
	padding the border of the input

parameter sharing - if we know one region feature is useful, when we update its weights through backprop, we can use the same weights for all the neurons having this feature

pooling layers - 
	downsamples the input image to reduce the dimensionality we are learning from
fully connected layers - 
	tries to produce class scores from the activations

operates on the ACTIVATION MAPS (Relu(x) where x is the kernel/filter?)
usually the max pooling layer has a kernel with dimensionality of 2x2 with a stride of 2

general pooling layers include:
	l1/l2 normalization
	average pooling
	
relu - is a non linear activation function used in every neuron to solve the problem of the vanishing gradient
	faster to compute than sigmoid or tanh

fully connected layer
![[Pasted image 20231115181302.png]]

### ways to architect

![[Screenshot 2023-11-15 at 6.12.43 PM.png]]
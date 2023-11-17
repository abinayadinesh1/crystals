used deep cnn’s to classify cultivars of chjinese chrysanthemum

**image net has a bias to classifying based off texture, not color** (which matters more in ag)

depending on what stage you take images of the plants at, abiotic factors, and opening periods, plants of the same cultivar can actually look very different

even within cultivar, there is a lot of room for variability

  

  

images

pngs

6,000 x 6000

each cultivar had only 2-3 representatives

  

  

  

bruh this was a labelled dataset

  

  

data augmentation

cant use color jitter or greyscale

rotation, flip, and symmetry also invalid

  

  

  

  

2018:

126 cultivars, 80 images from each, cropped then batch pathed for total of 80,640 images

  

  

2019 was the test dataset, lot of unseen cultivars

  

used resnet18, not pretrained, and not resnet50 (a deeper network) because they didnt have a lot of data

used 3 parallelax softmax classifiers to get feature representation of images

one to output cultivar name, flower type, and petal type

  

tested different learning rate adjustmets

standard decay strategy

step decay strategy

line decay strategy

poly decay strategy

  

  

  

feature exploration

affinity propogation - what features determined if two images would be in the same class or not? what is the affinity of one feature to another?

principal component analysis - used to figure out class separability of cultivars
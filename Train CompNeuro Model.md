# Action Items:
- train with all 108 numpy arrays resulting from Superglue alignment
	- this means to follow all the steps below with the full amt of arrays
- finish training the model with 50 numpy arrays - Abinaya
	- figure out how to resume model from checkpoint
### make the dataset: convert our numpy arrays to rgba and save as png
1. take the **numpy arrays** of images that you want and put them in the aligned folder in the Sandbox directory![[Screenshot 2023-11-13 at 12.37.01 PM.png]]
2. convert those numpy arrays to rgba using the npy_rgba notebook, located in the Sandbox directory
	![[Screenshot 2023-11-13 at 12.40.02 PM.png]]
3. Drag and drop the images that were outputted into the DIV2K folder
![[Screenshot 2023-11-13 at 12.44.55 PM.png]]

## train the model 
PLEASE USE GPU'S, OR ELSE THIS WILL TAKE ALL DAY
run the command:
python3 main.py --ons_dim 32 -nct 4


this will take all the images in DIV2K and batch them into a directory called DIV_2K_Cropped_37 so we have a dataset of 50k images
then it will automatically train the model on this dataset

## evaluate
evalute using the color matching functions:
python 2_color_matching.py

figures will be in results/cmf/model_3_tri_32_Cn_0.01


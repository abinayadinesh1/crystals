https://www.adept.ai/blog/fuyu-8b
supports images (at arbitrary resolutions), graphs, diagrams, ui, fine grain localization of images
answer questions based on images and caption images well

![[Screenshot 2023-10-24 at 11.24.54 PM.png]]



what is a knowledge worker?
needs to understand user context (what question are they asking, why are they on this page right now, what are they trying to do?)

their model is a decoder only transformer, no specialized image encoder
dont embed all the pictures, just insert the patch into the transformer


fuyu is a decoder only model, meaning ![[Screenshot 2023-10-24 at 11.55.49 PM.png]]
the encoder is like training the model for reconstruction of the task on a set of inputs/images. this doesnt fine tune on any dataset that way and instead relies on embeddings and goals. 

it bypasses the embedding lookup. just feed a patch of an image into the first layer of the transformer. 


raster scan order - they start at the top left of the screen and take patches up until the bottom right of the screen




what are the existing position embeddings? 
why dont u use pooling or causal attention?

they really dont agree with image understanding benchmarks
		the question answer benchmarks are terrible and not general at all. they ask for extremeley specific answers (honestly thats defeating the purpose of representation learning), and ARE LITERALLY SOMETIMES WRONG


capabilities of fuyu-8b
chart, diagram, and document understanding





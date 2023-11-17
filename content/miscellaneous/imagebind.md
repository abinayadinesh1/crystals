  

  

  

ImageBind could also provide a rich way to explore memories — searching for pictures, videos, audio files or text messages using a combination of text, audio, and image.

  

  

  

In typical AI systems, there is a specific embedding (that is, vectors of numbers that can represent data and their relationships in machine learning) for each respective modality. 

they make a create a **joint embedding space across multiple modalities** without needing to train on data with every different combination of modalities. 

  

representation learning - where models are trained to map high-dimensional data to lower-dimensional vector spaces

  

Word2Vec - has one embedding for one word

BERT + GPT get the meaning of words within the context of a sentence

  

CNNs give image embeddings

  

diff type of model architecture used to pick up important features from all these diff types of inputs 

  

  

**Network Analysis:** Embeddings have proven valuable in network analysis and graph-based machine learning. Graph embeddings represent nodes in a graph as low-dimensional vectors, capturing structural information and relationships between nodes. These embeddings enable tasks such as link prediction, community detection, and node classification. By mapping nodes to an embedding space, graph-based algorithms can efficiently analyze large-scale networks.

  

threw audio embeddings with a pretrained DALLE-2 decoder to work with CLIP text embeddings

  

  

Previously, learning such a joint embedding space for all modalities would require collecting all possible combinations of paired data — an infeasible feat.

**why is this true?**

have an embedding for grass and peaceful sounds, then grass and 

uniwue embeddings for grass with all the modalities: what is the sound of grass?

IMAGEBIND CAN TELL THIS WITH NO PRIOR TRAINING DATA.

  

  

  

large-scale vision-language models and extending their zero-shot capabilities to new modalities just by using their natural pairing with images

  

naturally paired self supervised data?

  

  

upgrade make a scene to generate images using audio sounds, such as laughter or rain.

  

While we explored six modalities in our current research, we believe that introducing new modalities that link as many senses as possible — like touch, speech, smell, and brain fMRI signals — will enable richer human-centric AI models.
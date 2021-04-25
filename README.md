# prose2sound
Calvin Lu (CL3644) & William Gu (XG2355)
================================================================================

---------------------------
Contents:
---------------------------
Within this repository are two python notebooks, several .sco & .wav files, and files relating to RTcmix. 
Text conversion to sound is done using either of the two notebooks: Sonification_Project.pynb & Sonification_Project_BERT.ipynb. It may be necessary to first download the Gutenberg Poetry Dataset from [here.](http://static.decontextualize.com/gutenberg-poetry-v001.ndjson.gz) The dataset is used to both train the Word2vec model and form the vocabulary with which we fit the PCA transform. Cells within the notebook can be run to train or load pretrained parameters for Word2vec and BERT models, fit PCA using a given corpus, generate embeddings for a given text, and convert the resulting PCA'd embeddings into sound. Several cells also calculate and display the explained variances of the components, but they are not necessary unless the sound generation method used scales amplitude by explained variance.

Of the included sound files, bert_repeat.wav may be of special interest as it demonstrates that when a sentence is composed of nothing but the same word repeated over and over, BERT's representations of the word in each location follows a periodic pattern. It may be difficult to observe this pattern in a visual representation, and it may be difficult to manually sift through pairwise calculations between every pair of locations in the data to observe the pattern quantitatively. While this specific example might not be of great importance, it demonstrates potential for use of sonification as a novel way of representing high-dimensional data. 
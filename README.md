# Stance Detection on Hansard Debate Corpus

The project aims to predict stance (for / against) label for a speech in the dataset given the motion.
Dataset: https://data.mendeley.com/datasets/xsvp45cbt4/2 

We have 3 notebooks
Stance_Detection.ipynb -> This contains differnet models trained for stance detection

We have used data augmentation to get additional training examples. This is done using
1. Word Embeddings (explained in Stance_Detection.ipynb)
2. Speech Generation (speech generation models are present in SpeechGeneration.ipynb)

Speech Generation models are trained on bigger Hansard corpus (https://evanodell.com/projects/datasets/hansard-data/). We wanted to train the model for a specific party, say SNP. Use transfer learining and retrain the learned weights to generate positive and negative utterances for each party. Then, retrain the Stance Detection models on the complete dataset. (transfer learning to generate new utterances not completed since we did not desired quality speeches with the trained models and need to improve the models).

We also wanted to train a multi-class classification model on the bigger Hansard corpus and use the model to classify newly generated speeches to evaluate both models. Classification model is present in  (not completed since could not train a good model with desired accuracy)

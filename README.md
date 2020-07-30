Lyrics Generator


Overview: This is a Deep learning model, which uses LSTM and is implemented through TensorFlow. Its main function is to generate Lyrics(text) upto "n" number of words for a given inpur line.

Files:

1) train_model.ipynb: This Jupyter notebook creates and trains the LSTM model. It has 2-Layer LSTM model followed by 2 Dense layers having total of 3.1M trainable params. The model achieves an accuracy of about 55%

2) lyrics_generator.ipynb: This jupyter notebook loads the model and predicts "n" (user input) of words for a given input line

3) lyrics.txt: This is a dataset of about 1000 English songs from various artists such as Adele, Britney Spears, Justin Beiber, Elvis presley, Rihanna and others. This file can be replaced to train the model on other datasets such as English Essays, Stories, chat conversations etc.


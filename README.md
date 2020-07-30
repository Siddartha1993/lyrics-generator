# Lyrics Generator 

## Overview: 
This is a Deep learning model, which uses LSTM and is implemented through TensorFlow. Its main function is to generate Lyrics(text) upto "n" number of words for a given input line.

## Files:

1) ### train_model.ipynb: 
    This Jupyter notebook creates and trains the LSTM model. It has 2-Layer LSTM model followed by 2 Dense layers having total of 3.1M trainable params. The model achieves an         accuracy of about 55%

2) ### lyrics_generator.ipynb: 
    This jupyter notebook loads the model and predicts "n" (user input) of words for a given input line

3) ### lyrics.txt: 
    This is a dataset of about 1000 English songs from various artists such as Adele, Britney Spears, Justin Beiber, Elvis presley, Rihanna and others. This file can be replaced       to train the model on other datasets such as English Essays, Stories, chat conversations etc.

## Model:

  The first layer of the model is the Embedding layer that vectorizes the input words and holds them into clusters of similar-meaning words. Next,The model uses 2 layers of LSTM. The first layer is Bidirectional Model having 256 nodes with a dropout of 0.2 and the other LSTM layer has 128 nodes. Next we have 2 dense layers having nodes equal to (total_number_of_words/2) and (total_number_of_words) respectively. Below is the summary of the model:
  
  

      Layer (type)                 Output Shape              Param #   
      =================================================================
       embedding (Embedding)        (None, 23, 100)           763400    
      _________________________________________________________________
      bidirectional (Bidirectional (None, 23, 512)           731136    
      _________________________________________________________________
      dropout (Dropout)            (None, 23, 512)           0         
      _________________________________________________________________
      lstm_1 (LSTM)                (None, 128)               328192    
      _________________________________________________________________
      dense (Dense)                (None, 3817)              492393    
      _________________________________________________________________
      dense_1 (Dense)              (None, 7634)              29146612  
      =================================================================

  ## Result:
  
   The **lyrics_generator.ipynb** file requires a input line from the user, continuing on which, the model will predict its own set of words.
   
   ### Example 1
   

   "I miss you"
   

    I miss you when the lights go out 
    from the rest who is standing there 
    i will sustain 
    closing down in your eyes 
    i see through the dark of your body 
    strikes a extra road outta lights
    know something the whole block on her name 
    i can't go back to the same old lane
    How could you come be true 
    i was wrong
    oh maybe i was burned but i called it a lesson learned
    i see your head don't do about you 
    darlin' i'll find someone to find you up my head


  ### Example 2
 

   "I will see you"

    I will see you out of control 
    don't you leave me thinking of me feeling this way i'm leaving myself 
    i wish i could lay down beside you 
    you see the way you look at me now 
    i'll be standing right next to you yeah yeah yeah yeah 
    closed there ain't nothing here for me 
    i'm full of mud on the wall sitting there 
    it is just you and i can't help myself from shining like a rocket that takes off the lights 
    lay me down pour it up pour it up pour it up all night on my soul



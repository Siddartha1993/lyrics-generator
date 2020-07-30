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
  
  
'''  
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
 '''
  ## Result:
  
   The **lyrics_generator.ipynb** file requires a input line from the user, continuing on which, the model will predict its own set of words.
   
   ### Example 1
   
'''
   "I miss you"
   
    I miss you when the lights go out 
    from the rest who is standing there 
    yeah uh i will sustain 
    close down in your eyes 
    i see through the dark of your body 
    strikes a extra road outta lights
    know something in the whole block on her name 
    i can't go back but the reeds are growing out of my fingertips 
    hall on the ground more than something slow oh tun hour band jump in the flames are lay across their minds 
    most squeezin' in coincidence 
    lancashire gats penny lane and the floor boils 
    i'll find someone to find you up my head
   
 ''' 
  ### Example 2
  
 '''
 "How could you" -


    How could you come be true i was wrong 
    oh maybe i was burned but i called it a lesson learned 
    i see your head don't do about you 
    darlin' gonna give me a flame let me photograph you 

    in this morning ain't gonna be me in my wall
    mj taught me to make a fool out of you 
    lost their moments straight up and the bath me in my throat 
    back once in the middle of the ground 
    train uh birthday and lonesome road adds up to take me open off the street 
 
 '''
 
  

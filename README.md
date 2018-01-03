# Bidirectional Recurrent Convolutional Networks for Disentangling Brain Activity from EEG Data

In this study a collected students' EEG brain activity while watching online courses (video clips) is used to train a classifier that detects when a student is confused. In doing so, a bidirectional recurrent convolutional networks classifier is used.

## Data:
A data set is from the 'EEG brain wave for confusion[1]'; EEG data from 10 students assigned to watch 20 videos, after each video, students rated their confusion level on a sclae of 1-7. These labels are quantized into two classes: (i) Confused, and (ii) Not confused
Table 1 shows the features of this data set.

<table style="width:100%">
  <tr>
    <th>Feature</th>
  </tr>
  
  <tr>
    <td>Attention - propriatary</td>
  </tr>
  <tr>
    <td>Meditation - propriatary</td>
  </tr>
  <tr>
    <td>Raw EEG signals</td>
    
  </tr>
  <tr>
    <td>Theta frequency band</td> 
  </tr>
    <tr>
    <td>Alpha 1 frequency band</td> 
    </tr>
     <tr>
    <td>Alpha 2 frequency band</td> 
    </tr>
    <tr>
    <td>Beta 1 frequency band</td>
    </tr>
     <tr>
    <td>Beta 2 frequency band</td> 
    </tr>
    <tr>
    <td>Gamma 1 frequency band</td>
    </tr>
     <tr>
    <td>Gamma 2 frequency band</td> 
    </tr>

## Model: 
Bidirectional recurrent convolutional networks classifier with the following stricture is used for this study:



_________________________________________________________________
Layer (type)                 Output Shape              Param #   
=================================================================
time_distributed_379 (TimeDi (None, None, 140, 7, 20)  520       
_________________________________________________________________
dropout_253 (Dropout)        (None, None, 140, 7, 20)  0         
_________________________________________________________________
time_distributed_380 (TimeDi (None, None, 70, 3, 20)   0         
_________________________________________________________________
time_distributed_381 (TimeDi (None, None, 4200)        0         
_________________________________________________________________
lstm_305 (LSTM)              (None, None, 10)          168440    
_________________________________________________________________
dropout_254 (Dropout)        (None, None, 10)          0         
_________________________________________________________________
bidirectional_53 (Bidirectio (None, None, 40)          4960      
_________________________________________________________________
lstm_307 (LSTM)              (None, 10)                2040      
_________________________________________________________________
dense_127 (Dense)            (None, 1)                 11        
=================================================================
Total params: 175,971
Trainable params: 175,971
Non-trainable params: 0
_________________________________________________________________


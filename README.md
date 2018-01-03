<img src="https://github.com/favicon.ico" width="48">![alt text](screenshots/filename.png "Description goes here")# Bidirectional Recurrent Convolutional Networks for Disentangling Brain Activity from EEG Data

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

 
(style="width:100%" model_plot.png "Figure 1")

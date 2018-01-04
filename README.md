# Bidirectional Recurrent Convolutional Networks for Disentangling Brain Activity from EEG Data

In this study a collected students' EEG brain activity while watching online courses (video clips) is used to train a classifier that detects when a student is confused. In doing so, an optimized bidirectional recurrent convolutional networks classifier is used.

## Data
A data set is from the 'EEG brain wave for confusion[1]'; EEG data from 10 students assigned to watch 20 videos, after each video, students rated their confusion level on a sclae of 1-7. These labels are quantized into two classes: (i) Confused, and (ii) Not confused
Table 1 shows the features of this data set.

<table style="width:50%">
  <caption>Table 1. EEG brain wave for confusion[1]</caption>
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
    </table>

## Model
Bidirectional LSTM networks with convolutional layer to extract the siganl features is used as a classifier with the arcitecture illsutrated in Fig. 1, is used in this study:

<p align="center">
  <img src="model_plot.png" width="500"/>
  <figcaption>Figure 1 : Model Architecturee</figcaption>
</p>

## Result
Here, a trained classifieres on the data from all but one student, is tested on the held-out student. 
The procedure is performed for each student and the acciracy of the classificatio is presented in Figure 2 

<p align="center">
  <img src="EndResulst.jpg" width="500"/>
  <figcaption>Figure 2 : Experiment-based and Averageaccuracy </figcaption>
</p>


Figure 3 and Figure 4 show the recently published results using the same dataset and accuracy metrics.

<p align="center">
  <img src="REF-1.jpg" width="500"/>
  <figcaption>Figure 3 : Illustrated results in [1] </figcaption>
</p>

<p align="center">
  <img src="REF-2.jpg" width="500"/>
  <figcaption>Figure 4 : Illustrated results in [2] </figcaption>
</p>

## Code
<p><a href="DNNforEEFSignals.ipynbDNNforEEFSignals.ipynb"> The code is presented here </a></p>


## Refrences
[1] Wang, Haohan, Yiwei Li, Xiaobo Hu, Yucong Yang, Zhu Meng, and Kai-min Chang. "Using EEG to Improve Massive Open Online Courses Feedback Interaction." In AIED Workshops. 2013.

[2] Ni, Zhaoheng, Ahmet Cem Yuksel, Xiuyan Ni, Michael I. Mandel, and Lei Xie. "Confused or not Confused?: Disentangling Brain Activity from EEG Data Using Bidirectional LSTM Recurrent Neural Networks." In Proceedings of the 8th ACM International Conference on Bioinformatics, Computational Biology, and Health Informatics, pp. 241-246. ACM, 2017.

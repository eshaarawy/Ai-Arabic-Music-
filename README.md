# Deep Learning Project 

## Install
This project requires Python 3.x and the following libraries installed:
NumPy
Pandas
matplotlib
os
pickle
librosa
pydub
soundfile
io
Keras
Tensorflow
We got access to all of that by using Anaconda.
## Data Collecting & Preprocessing.
We started by collecting Arabic music data for about 11 different composers, totaling approximately 256 files ranging from 3 to 55 minutes each. After collecting this vast amount of data, we began our first task, which involved preprocessing the data through a pipeline of tasks:

1- Segment the large files.

2- Convert them to WAV format.

3- Segment the WAV files into smaller pieces.

4- Normalize the audio data.

5- Extract MFCCs (Mel Frequency Cepstral Coefficients) in the form of NumPy arrays for the first and second experiments in the classification task.

6- Extract Mel-Spectrograms for the third, fourth, and fifth experiments and log-spectrograms for the generation task.

7- Plot the spectrograms to observe the trends.

## Classification task

For the classification task, we employed several approaches to improve the accuracy of our model. 

1- In the first experiment, we used non-evenly distributed data with MFCC as input and a model architecture consisting of two con2d layers to classify the data into 11 categories. This experiment resulted in a test accuracy of 0.5489017367362976.

2- In the second experiment, we modified the architecture used in the first experiment to achieve better validation and testing accuracy. Additionally, we used evenly distributed data in this experiment, which resulted in a higher test accuracy of 0.5595895648002625.

3- In the third experiment, we changed the form of the input to mel spectrograms, which are capable of representing more features, thereby aiding the model in learning and leading to improved results. This experiment resulted in a test accuracy of 0.6252723336219788.

4- To further improve our model's accuracy, we used data augmentation techniques in the fourth experiment to increase the size of our data and repeated experiment three. This led to a better accuracy, with a test accuracy of 0.6758170127868652.

5- Finally, in the fifth experiment, we used the same approach as in experiment two but with an increase in the augmented data. This resulted in a significant improvement in accuracy, with a test accuracy of 0.7315903902053833.

## Generation Task
1- Our data preprocessing involved a well-defined pipeline, starting with segmenting the audio files into 5.94-second intervals, padding if necessary, and extracting log spectrograms for model training. We then applied min-max normalization for post-processing and saved the preprocessed data in the specified paths. As an additional step, we also extracted log spectrogram images to observe music trends in terms of frequency and time. In total, we preprocessed 75 WAV files, resulting in 8756 segments.

2- To generate new music data from our classical music dataset, we utilized a VAE architecture comprising an Encoder, Bottleneck, and Decoder. Both the Encoder and Decoder consisted of 5 convolutional layers, resulting in millions of parameters for the model. .......to be completed soon 

# Neural-Network-BCI

Team Members
The Team is composed of Ulas Ayyilmaz, Yotam Twersky, Colin Kirkpatrick. We believe our strengths complement each other. We have different permutations of our team that are more experienced with Neural Networks, with implementing SciKit-Learn in python, with Neuroscience concepts, data collection practices and administering the EEG.
Summary
Our project is evaluating the possibility of using a (likely convolutional) Neural Network to predict human movement in real time through a live Brain Computer Interface (BCI). We know it sounds ambitious due to the scope of it as well as the fact that we are gathering our own data building and optimizing a model and doing the application step on our own. We will be gathering data using an EEG which our team members will be using. The great thing is that the data we are getting will just be time series and allows us to get one person to generate hundreds of examples. We will create a video in advance for people to follow and that data will have a consistent label based on the timestamp. Each electrode on the EEG device has its own time series of electrical activity so we will line these up as our features with each example being a time-stamp (average over a chunk). Ideally we will be able to demonstrate the use of the neural network for predicting human movements by creating a video showing the real time BCI that demonstrates live classification of real time brain waves. If this is not possible then we can do more of a standard analysis on a train test split to evaluate the effectiveness of our model for this use case.
Data Collection
The original data that we are collecting consists of electrical activation (y- represented by sinusoidal waves) and time series (x- tracked by milliseconds). We will divide the EEG graph into distinct time sections(most likely separated by 5 seconds) representing the duration of time when the participants will be moving their hands. We will calculate the average activation (y-axis) per time section, and feed that average activation value-label combination to our neural networks. As stated in summary, we will have multiple electrodes recording activity. The electrodes which are associated with the Primary Motor Cortex on both hemispheres will be of most significance.
Dummy Data
TimeStamp Chunk
Electrode 1 avg
Electrode 2 avg
Activity Label
0-5 seconds
60Hz
60Hz
None
5-10 seconds
500Hz
60Hz
Right
10-15 seconds
62Hz
59Hz
None
15-20 seconds
59Hz
500Hz
Left




Model
We will use a 1D CNN. The input layer will have one input node for each electrode. Each example feature will represent the timestamp chuck average for one electrode. We will experiment with layers and numbers of hidden nodes. Our output layer will contain three nodes. One each for left, right and neither. We will classify based on which output node has the highest value. 

Resources

We will train a convolutional neural network on our time-series data. This may require some amount of wrapping on either end in order to facilitate our particular needs. However, for the CNN itself, we intend to use a model sourced from SciKitLearn. Because our project is more heavily concerned with creating the computer-brain interface itself, this should be a relatively small part of our total work. 
In addition to the CNN, we will be using the aforementioned EEG tools from the neuro department. This will include Lab Streaming Layer Pandas, Numpy. 

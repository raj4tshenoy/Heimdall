# Heimdall
by Hexall Tech


PROJECT Heimdall :A Natural disaster prediction and warning system by Hexall Tech.

# Short Note:

Team members: [Rajat Shenoy](https://github.com/raj4tshenoy) ,[Avi Solanki](https://github.com/Avi-141) ,[Roshan Jacob](https://github.com/roshan1999).

# Goal :
To predict the probability of occurence of an Aftershock with 80% or more accuracy and to cater to the needs of the people affected by the disaster through our app or SMS.

Technologies used: Flutter, Scripts coded in Python, Matlab , Deep Learning, Tensorflow, Keras UGCS urls, Twilio API, Flask, Firebase, Azure AppServices, JavaScript, HTML, LeafletJS
Work Flow:

Our Deeplearning model gets data input from realtime sources at specific intervals. In case an Aftershock is predicted, an SMS broadcast is sent to concerned authorities and locals. The Application is a Disaster Helpline / Relief application which can be used by people to contact authorities and help authorities to conduct necessary actions. The App has multiple features such as SOS and Missing person, which alert the authorities to initiate a relief or search operation. Users can also send an SMS to our phone number if they do not have internet access to make use of the same features.
ABSTRACT:

Predicting and managing earthquakes is indeed a difficult task , since the seismic readings play a vital role in the same.We would be creating a model to accurately classify these disasters based on real time data . The main idea,isn ot to go for the Earthquake prediction before time using Time series,RNN's or LSTMS But to look at the other aspect of the aftereffects of an earthquake and the aftershocks it brings with it . If we are able to predict the after shocks and predict the location , we would be able to warn all people in a particular radius of interest.

Further , Tsunamis which follow after earthquakes can also be predicted but have not been discussed in the project .
# MOTIVATION BEHIND THE IDEA:
AFTERSHOCK SAVE:

Currently people have been using the coulomb's stress criterion to explain the spatial distributions of aftershocks, but sometimes patterns go unnoticed . Aftershocks are a response to changes in stress generated by large earthquakes and represent the most common observations of the triggering of earthquakes. The deep-learning model that we have developed are trained and tested using co-seismic slip distributions from the SRCMOD online database of finite-fault rupture models.(FSP format files)
# DEEP LEARNING MODEL :

The output of this final neuron may be interpreted as the predicted probability that a grid cell generates one or more aftershocks.We assess the accuracy of the neural-network aftershock location forecasts on the test dataset using receiver operating characteristic analysis. The merged AUC value across all slip distributions and grid cells in the test dataset for our neural-network forecast is 0.8445, which is larger than that of Coulomb failure stress criterion which has been done previously .
The algorithm:

The idea is to observe a volume which extends by

1.'K' kms horizontally

2.'V' km vertically from the main shock.

In our network , K is 100 and V is 50.

1.Distribute the volume into 5km x 5km x 5km small volumes. 2.Elastic 'stress change tensors' at each of their centroid. 3.Predict whether there was an aftershock in that small volume or not. 4.In order to know the ground truth we use International Seismological Center (ISC) event catalogue, in which for each main shock we looked up for its corresponding aftershocks from 1 sec to 1 year time and using that information we created our ground truth i.e. whether there was an aftershock in that small volume or not. Binary classificcation of an aftershock . Aftershock and aftereffects prediction is the final output
Data from SRCMOD(public dataset)

http://equake-rc.info/SRCMOD/searchmodels/allevents/

The data source above is of the Finite rupture source form which has been convereted to a CSV file , whose scripts will not be discussed in this repository. The data provided by the SCRMOD file contains the information about the hypocenter, latitude, longitude, magnitude, strike, dip, the inversion parameters and many other relevant data that is sufficient to get an insight of the earthquake and the stress patterns.
Outputs and summary:

The network,tries to extract the important features in order to predict the whether there is a chance of having an aftershock. For this project we use two activation functions TANH and RELU.The ouput is a sigmoid one , for a probabilistic output between 0 to 1. Evaluating the trained model gives us a roc_auc score of 0.8445. Epochs:300 Batch size:4000
Other references of use:

# 1.Study material:
http://www.bosai.go.jp/study/application/dc3d/DC3Dhtml_E.html

# 2.Research paper:
https://eost.unistra.fr/fileadmin/upload/EOST/Zacharie_Duputel/Papiers/DeVries_et_al2018.pdf

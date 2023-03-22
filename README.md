# Modeling Charity Projects with Neural Networks

## Overview

We look at a large dataset of charity funding data. Using this data we develop a variety of neural network models in an attempt to predict the success of a potential project.

## Results

Data Preprocessing:
- Our target variable for the analysis is the "IS_SUCCESFUL" dimension which tracks the eventual success or failure of each project.
- The EIN and NAME columns are identifyer information which may be informative when digging into the data, but aren't relevant for our model, so we do not conisder them as features for our models.
- The remainging dimensions are what we take as features as our model: Application_type, affiliation, classification, use case, organization, status, income amount, special considerations, and asking amount.

Model Structures and Results. All models trained for 100 epochs.
- For our first model we used two hidden layers, one with 7 neurons, and one with 5, using relu activation for the hidden layers and sigmoid for the outputs. With this model, we achieved an accuracy of ~72.52%

![](https://raw.githubusercontent.com/SecretDoves3000/Neural_Network_Model_Charity_Analysis/main/images/m1SS.png)

![](https://raw.githubusercontent.com/SecretDoves3000/Neural_Network_Model_Charity_Analysis/main/images/m1aSS.png)

- For our first optimization attempt was adding more neurons, with 10 in the first layer and 7 in the second. This attempt achieved an accuracy of ~72.2%.

![](https://raw.githubusercontent.com/SecretDoves3000/Neural_Network_Model_Charity_Analysis/main/images/m2SS.png)

![](https://raw.githubusercontent.com/SecretDoves3000/Neural_Network_Model_Charity_Analysis/main/images/m2aSS.png)

- For our second optimization, we return to the original neuron structure, but we use sigmoid activiations in all layers. This model achieved an accuracy of ~72.81%

![](https://raw.githubusercontent.com/SecretDoves3000/Neural_Network_Model_Charity_Analysis/main/images/m3SS.png)

![](https://raw.githubusercontent.com/SecretDoves3000/Neural_Network_Model_Charity_Analysis/main/images/m3aSS.png)

- For our final attempt, we add a third hidden layer of 11 neurons using sigmoid activation functions. This model achieved an accuracy of ~72.54%

![](https://raw.githubusercontent.com/SecretDoves3000/Neural_Network_Model_Charity_Analysis/main/images/m4SS.png)

![](https://raw.githubusercontent.com/SecretDoves3000/Neural_Network_Model_Charity_Analysis/main/images/m4aSS.png)

## Summary

Looking at our attempts, it seems that a neural network model of our data, without any extra manipulation of the data, achieves an accuracy of 72-73%. To push beyond that into the >75% range we should conisder looking deeper into our data to find insiginificant factors or outliers which may be making this model too difficult to fit. Also, given that we are splitting our data into two subsets, successful and unsuccessful, we may have more success with an unbalanced logistic regression machine learning model. This may have trouble with the high dimension of our dataset, but given that we are already considerign dropping some factors, it should be given consideration.

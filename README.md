# Modeling Charity Projects with Neural Networks

## Overview

We look at a large dataset of charity funding data. Using this data we develop a variety of neural network models in an attempt to predict the success of a potential project.

## Results

Data Preprocessing:
- Our target variable for the analysis is the "IS_SUCCESFUL" dimension which tracks the eventual success or failure of each project.
- The EIN and NAME columns are identifyer information which may be informative when digging into the data, but aren't relevant for our model, so we do not conisder them as features for our models.
- The remainging dimensions are what we take as features as our model: Application_type, affiliation, classification, use case, organization, status, income amount, special considerations, and asking amount.

Model Structures and Results
- 
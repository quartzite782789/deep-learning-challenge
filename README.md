# deep-learning-challenge
Challenge 21
 Copilot, ChatGPT, and classmate assistance were used to in the generation of this code.

# Overview

The purpose of the analysis was to develop a model to identify applicants for funding that have the best chance to use the money effectively. The model is based on a dataset from more than 34,000 organizations with the IS_SUCCESSFUL being used to look at the combination of features that lead to effective use of funds.

# Results

What variable(s) are the target(s) for your model?
**IS_SUCCESSFUL**

What variable(s) are the features for your model?
1. APPLICATION_TYPE
2. AFFILIATION
3. CLASSIFICATION
4. USE_CASE
5. ORGANIZATION
6. INCOME_AMT
7. SPECIAL_CONSIDERATIONS
8. ASK_AMT
9. STATUS

What variable(s) should be removed from the input data because they are neither targets nor features?

**EIN**: This is just an identifier and would have no bearing in the predictions
**NAME**: This is just an identifier and would have no bearing in the predictions        


## Compiling, Training, and Evaluating the Model
How many neurons, layers, and activation functions did you select for your neural network model, and
why?

**Initial run:**

Number of layers: 2

Neurons in layer 1: 16
Neurons in layer 2: 16
Activation in layer 1: ReLu
Activation in layer 2: ReLu
Activation in output layer: Sigmoid

**First Optimazation run:**

Number of layers: 3

Neurons in layer 1: 128
Neurons in layer 2: 64
Neurons in layer 3: 32
Activation in layer 1: ReLu
Activation in layer 2: ReLu
Activation in layer 3: ReLu
Activation in output layer: Sigmoid

**Second and Third Optimazation runs:**

Number of layers: 3

Neurons in layer 1: 160
Neurons in layer 2: 64
Neurons in layer 3: 32
Activation in layer 1: ReLu
Activation in layer 2: ReLu
Activation in layer 3: ReLu
Activation in output layer: Sigmoid

Were you able to achieve the target model performance? **No**

What steps did you take in your attempts to increase model performance?

Increased number of layers
Increased number of neurons
Used PCA to reduce noise and reduce features from 43 to 32
Increased Epochs with early stop

## Summary

Overall, the model was not successful and unable to get past a 73% accuracy rate. A change in the activation may have resulted in a higher accuracy.

Other options to improve the model include train longer, add drop out to stabilize training and perhaps improve generalization or rebalancing weights.
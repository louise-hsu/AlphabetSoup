# AlphabetSoup 


## Project Overview 
Understand machine learning using unsupervised algorithms, which is used when we are not sure what we are lookig for.

This module has taught me the following:

1. Building Neural Networks
2. Preparing Neural Netowkr Datasets
3. Digging Deeper in Neural Networks
4. Selecting the Best Model for Dataset
5. Exporting and Importing Trained Models

        
## Documents

- AlphabetSoupChallenge.ipynb : challenge
- charity_data.csv : raw data
- README.txt : Module summary and addresses questions


# Module 19 Challenge 

## Challenge Summary
build your own machine learning model that will be able to predict the success of a venture paid by Alphabet soup. Your trained model will be used to determine the future decisions of the company—only those projects likely to be a success will receive any future funding from Alphabet Soup.

## Challenge overview

1. Import, analyze, clean, and preprocess a “real-world” classification dataset.
2. Select, design, and train a binary classification model of your choosing.
3. Optimize model training and input data to achieve desired model performance.

## Summary/Questions

### What variable(s) are considered the target for your model? 
IS_SUCCESSFUL
### What variable(s) are considered to be the features for your model? 
AFFILIATION, CLASSIFICATION, USE_CASE, ORGANIZATION, INCOME_AMT, SPECIAL_CONSIDERATIONS, ASK_AMT, APPLICATION_TYPE, STATUS
### What variable(s) are neither and should be removed from the input data? 
EIN and NAME


### How many neurons and layers did you select for your neural network model? Why?

I selected 2 layers and a total of 130 neurons. I chose two layers because usually more layers lead to better performance. I did test with one layer and the predictive accuracy was a little lower compared to two layers. With more than two layers, I saw no significant increase in predicitive accuracy. I selected 130 neurons because there was a total of 43 features. The number of neurons should be about 2-3 times the number of features, which three times of 43 is 129. The first layer contains 26 and the second layer contains 5, which is the total of 130 neurons. 

### Were you able to achieve the target model performance? What steps did you take to try and increase model performance?

I was unable to achieve the target model performance of 75%. The model performance I would receive is 72-73% as the model performance. I did try different steps to increase the model performance, however it maxed our around 73%. 

If you looked at my blocked out code, I tried up to 3-4 inner layers. More than two layers did not make a significant change. I also tested model types -sigmoid, tanh, etc. in each layer. Relu was the best choice for each layer, with the output layer being sigmoid. Tanh was still comparable to relu. Moreover, I experiemented with the epoch value up to 100. I noticed around 20 times, the values did not change/increase by much, so I kept the epoch value at 20.The epoch of 100 decreased the model performance because too many epochs will cause overfitting. I played around with the neuron number as well. Depending on what the numbers I would change them to, it would either give almost the same performance number or decrease. 

### If you were to implement a different model to solve this classification problem, which would you choose? Why?

If I were to implement a different model to solve this classification problem, I would choose a random forest classifier because this model is easy to interpret and can handle outliers and nonlinear data. This data also does not have any tabular data, so the random forest classifier can be used. The results for a random forest is very comparable to deep learning - please see the last cell of code to see the model performance using the random forest classifier.

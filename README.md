# Neural_Network_Charity_Analysis

## Overview of the analysis: 

In this challenge, I was provided a dataset to preprocess and clean in order to be ran through a deep learning model that Deliverable 1 and 2 had me create. The intended accuracy of this model was below 75%. The purpose of this analysis is to practice processing data for machine learning as well as practice creating neural networks and machine learning models. In deliverable 3, I was instructed to make three attempts at optimizing the previously created model and increase the accuracy to above 75%. I was also working to answer the following questions:

### Data Preprocessing
- What variable(s) are considered the target(s) for the model?
- What variable(s) are considered to be the features for the model?
- What variable(s) are neither targets nor features, and should be removed from the input data?

### Compiling, Training, and Evaluating the Model
- How many neurons, layers, and activation functions were selected for the neural network model, and why?
- Was the target model performance achieved?
- What steps were taken take to try and increase model performance?


## Results: 
The analysis performed found that:

### Data Preprocessing
- What variable(s) are considered the target(s) for the model?
The variable that was considered the target for my model was the "IS_SUCCESSFUL" column.
- What variable(s) are considered to be the features for the model?
The "APPLICATION_TYPE", "AFFILIATION", "CLASSIFICATION", "USE_CASE", "ORGANIZATION", "STATUS", "INCOME_AMT", "SPECIAL_CONSIDERATIONS", AND "ASK_AMT" columns were used as the features for the model.

1
The image above shows the code used to create the features and target variables for the model.

- What variable(s) are neither targets nor features, and should be removed from the input data?
The "EIN" and "NAME" columns were unnecessary for analysis so they were dropped from the DataFrame.

2
The image above shows the code used to drop the two columns from the dataframe. 

### Compiling, Training, and Evaluating the Model
- How many neurons, layers, and activation functions were selected for the neural network model, and why?
I used eight neurons in the first hidden layer and five neurons in the second hidden layer. I used these numbers because it was what was successful in the last neural network I created. I wanted to try this first and see how it performed.

3
The above image shows the code used to create the neural network and view the structure.

- Was the target model performance achieved?
No, target accuracy was 75%. My model achieved 71%.

4
The above image shows the evaluation of the model performance.
- What steps were taken take to try and increase model performance?

Attempt One:
I first tried to remove the additional variable, "ASK_AMT." My initial thinking was that because it was so much larger, it was probably throwing off the model and I wanted to see if there was a big difference without it. 

5
The above image shows the code used to remove the "ASK_AMT" column.

I also lowered the number of bins used for the application type column by increasing the the threshold for unique values.

6
The above image shows the code used to reduce the number of bins for "APPLICATION_TYPE"

Lastly, I increased the number of neurons to twenty on the first hidden layer and 10 on the second hidden layer thinking that this would increase the accuracy of my model. 

7
The above image shows the code used to increase the number of neurons in each hidden layer.

Result of Attempt One: The accuracy was slightly higher and the loss was much lower.

8
The above image shows the evaluation of Attempt One.





## Summary: 
Summarize the overall results of the deep learning model. Include a recommendation for how a different model could solve this classification problem, and explain your recommendation.
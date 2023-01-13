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

![1](https://user-images.githubusercontent.com/111570965/212380280-9aea4899-2027-4914-a1ec-d3e835709705.png)


The image above shows the code used to create the features and target variables for the model.

- What variable(s) are neither targets nor features, and should be removed from the input data?

The "EIN" and "NAME" columns were unnecessary for analysis so they were dropped from the DataFrame.

![2](https://user-images.githubusercontent.com/111570965/212379311-830a4323-9988-4a7d-b725-982f01c04edc.png)

The image above shows the code used to drop the two columns from the dataframe. 

### Compiling, Training, and Evaluating the Model
- How many neurons, layers, and activation functions were selected for the neural network model, and why?

I used eight neurons in the first hidden layer and five neurons in the second hidden layer. I used these numbers because it was what was successful in the last neural network I created. I wanted to try this first and see how it performed.

![3](https://user-images.githubusercontent.com/111570965/212379339-b6f8f13a-d5f6-4f9f-93ac-1e032664f8fa.png)

The above image shows the code used to create the neural network and view the structure.

- Was the target model performance achieved?

No, target accuracy was 75%. My model achieved 71%.

![4](https://user-images.githubusercontent.com/111570965/212379397-496303d2-1aa1-41de-b731-3481fbd1f6eb.png)

The above image shows the evaluation of the model performance.

- What steps were taken take to try and increase model performance?

Attempt One:

I first tried to remove the additional variable, "ASK_AMT." My initial thinking was that because it was so much larger, it was probably throwing off the model and I wanted to see if there was a big difference without it. 

![5](https://user-images.githubusercontent.com/111570965/212379477-d50bc4b5-8987-4ead-bead-a48d99a422f7.png)

The above image shows the code used to remove the "ASK_AMT" column.

I also lowered the number of bins used for the application type column by increasing the the threshold for unique values.

![6](https://user-images.githubusercontent.com/111570965/212379494-28bd26c5-c343-41f4-8172-084f4b471059.png)

The above image shows the code used to reduce the number of bins for "APPLICATION_TYPE"

Lastly, I increased the number of neurons to twenty on the first hidden layer and 10 on the second hidden layer thinking that this would increase the accuracy of my model. 

![7](https://user-images.githubusercontent.com/111570965/212379508-a491b20b-aee1-4320-88b9-602472765ead.png)

The above image shows the code used to increase the number of neurons in each hidden layer.

Result of Attempt One: 72% accuracy

![8](https://user-images.githubusercontent.com/111570965/212379531-abd5a947-b2ad-4bb2-b13a-1ae098424c7c.png)

The above image shows the evaluation of Attempt One.

Attempt Two:

For this attempt, I decided to try a different activation function, "tanh" instead of "relu." Knowing that these two were the most complex of the activation functions, I thought this could perhaps increase the accuracy of my model.

![9](https://user-images.githubusercontent.com/111570965/212379545-17ce3a21-10b6-463b-b715-7ac776522071.png)

The above image shows the code used to run the model with the "tanh" function.

Result of Attempt Two: 72%

![10](https://user-images.githubusercontent.com/111570965/212379565-23db39ff-df6d-4c93-82dd-0fa4d3ca9593.png)

The above image shows the evaluation of Attempt Two.

Attempt Three:

For my final attempt, I wanted to see if adding another hidden layer would increase the accuracy of my model.

![11](https://user-images.githubusercontent.com/111570965/212379583-4babb747-4675-4284-bcea-de9184d5e949.png)

The above image shows the code used to add another hidden layer with 5 neurons to the model.

I also increased the epochs slightly to see if that would make a difference.

Result of Attempt Three: 72% accuracy

![12](https://user-images.githubusercontent.com/111570965/212379603-84a08c89-21af-4588-b0a9-1f4496509071.png)

The above image shows the code used to evaluate the model.

## Summary: 
Increasing the complexity of my model did not increase the accuracy as I thought it would. What I have learned from this challenge is that I need to keep working and practicing with deep learning models and obtain familiarity with how to chose the best model for each dataset. 

I would recommend scaling the "ASK_AMT" column down to match the rest of the dataset. Have that be the only change after the initial model was created and notate any changes. If this did not increase the accuracy over 75%, then I would want to make the model less complex and make changes slowly and make note of what changes occur with each optimization. 

I do not have enough experience with these models to make an official recommendation, but I would work on optimizing the model until the desired results are achieved and keep extensive notes of the process in order to utilize what was learned in later projects.

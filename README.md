# *Neural_Network_Charity_Analysis*

### Overview of the analysis:

Using machine learning and neural networks, create a binary classifier that is capabale of predicting whether
applicants will be successful if funded by Alphabet Soup.
    
    o Resources:  CSV file containing 34,000+ organizations that have received funding over the years.

### Results: 

#### Data Preprocessing

    1. What variable(s) are considered the target(s) for your model?
        - The IS_SUCCESSFUL was the variable chosen and used for the model.
    
    2. What variable(s) are considered to be the features for your model?
        - Every column but the IS_SUCCESSFUL, which was dropped, is our variable for the model. 
    
    3. What variable(s) are neither targets nor features, and should be removed from the input data?
        - We removed the EIN and NAME columns from our dataset becuase they had no impact on the outcome.

#### Compiling, Training, and Evaluating the Model

    1. How many neurons, layers, and activation functions did you select for your neural network model, and why?
        
        - Our first attempt to run the neural network we used 80 and 30 neurons with two hidden netowrks.
        The input activation chosen was "relu" and output was "sigmoid".  The results were less then
        satisfactory with a loss of 85% and an accuracy of 53%.
        
    <p align="center"><img src="https://github.com/PJ427/Neural_Network_Charity_Analysis/blob/main/Images/ASC.PNG"></p>    
        
    2. Were you able to achieve the target model performance?
            
        - The model was not able to achieve the 75% target
    
    3. What steps did you take to try and increase model performance?
    
        To try and optimize our model to achieve the 75% accuracy threshold the following was completed:
        
        - Removed additional variables.  In this case we remvoed the USE_CASE.

        - Additional neurons were added.  The first attempt to optimize, we increased the neurons to 100 and
        50 respectively. All other data remained the same and our results returned poorly, though improved
        somewhat.  Our loss dropped to 64% and our accuracy rose to 64%.
        
        <p align="center"><img src="https://github.com/PJ427/Neural_Network_Charity_Analysis/blob/main/Images/ASC_1.PNG"></p>
            
        - Next we added an additional hidden layer.  Since we orignally raised our neurons by 20, we set this
        layer at 20.  Input and output activation remained the same.  This result was still poor with a 69% 
        loss and 54% accuracy.
        
        <p align="center"><img src="https://github.com/PJ427/Neural_Network_Charity_Analysis/blob/main/Images/ASC_2.PNG"></p>
        
        - Finally, we changed the activation function of the output layer to better the optimization. The
        activation output to "linear", all other data from the 3rd test remained the same.  This resulted in
        our worse run of the model yet ending up with a loss of 2.764 and a 48% accuracy.
        
        <p align="center"><img src="https://github.com/PJ427/Neural_Network_Charity_Analysis/blob/main/Images/ASC_Final.PNG"></p>
    
### Summary:

Since running the model four times, through various modifcations, didn't produce the results we needed we have to look at what we can
do to reach our desired results.  Our best result came from adding additional neurons so we could simply try to make more adjustments
there by increasing the neurons and maybe chaning the input and/or output activation to achieve optimal results.  We could change the
model and use the random forest.  The random forest is a powerful model that can train on the large dataset and predict values quicker.
It combines multiple smaller models into a more robust and accurate model and uses a number of weak learner algorithms and combine their
output to make a final classifcation decision.  Both output and feature selection are easy to interpret, and they can easily handle
outliers and nonlinear data.  

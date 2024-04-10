# deep-learning-challenge
**Analysis Report on Alphabet Soup Charity Optimization.**

**Overview of the analysis: Explain the purpose of this analysis.
Data Preprocessing**

**1. What variable(s) are the target(s) for your model?**
Ans: The target for the model in all the three files and models is the column "IS_SUCESSFUL".

**2. What variable(s) are the features for your model?****
Ans:
A. Starter_Code.ipynb :
There are 43 variables used as the features in the original Starter code. This includes columns Status, Ask_amnt, ApplicationType_other, Application_type_T10, Application_type_T19, Application_Type_T3,Application_Type_T4, Application_Type_T5,Application_Type_T6,SPECIAL_CONSIDERATIONS_1-9999,SPECIAL_CONSIDERATIONS_10000-24999,SPECIAL_CONSIDERATIONS_100000-499999,SPECIAL_CONSIDERATIONS_10M-50M, SPECIAL_CONSIDERATIONS_1M-5M, SPECIAL_CONSIDERATIONS_25000-99999, SPECIAL_CONSIDERATIONS_50M+, SPECIAL_CONSIDERATIONS_5M-10M, INCOME_AMT_N ,INCOME_AMT_Y
B. AlphabetSoupCharity.ipynb
The same 43 variable as used in Starter Code are used as features in the attempt for optimization in the model for the file AlphabetSoupCharity
C. AlphabetSoupCharity_Optimization.ipynb
The last attempt for the optimization was made with some modification to the features. There are 42 features after some modification. This includes ASK_AMT, APPLICATION_TYPE_Other, APPLICATION_TYPE_T19, PPLICATION_TYPE_T3, APPLICATION_TYPE_T4, APPLICATION_TYPE_T5,APPLICATION_TYPE_T6, AFFILIATION_CompanySponsored, AFFILIATION_Family/Parent SPECIAL_CONSIDERATIONS_1-9999SPECIAL_CONSIDERATIONS_10000-24999, SPECIAL_CONSIDERATIONS_100000-499999,SPECIAL_CONSIDERATIONS_10M-50M,SPECIAL_CONSIDERATIONS_1M-5M, SPECIAL_CONSIDERATIONS_25000-99999, SPECIAL_CONSIDERATIONS_50M+,SPECIAL_CONSIDERATIONS_5M-10M,INCOME_AMT_N,INCOME_AMT_Y
**D. What variable(s) should be removed from the input data because they are neither targets nor features?**
I have removed the variable 'STATUS' as it does not affect the features or the targets.

**Compiling, Training, and Evaluating the Model**

**How many neurons, layers, and activation functions did you select for your neural network model, and why? Were you able to achieve the target model’s performance?
What steps did you take in your attempts to increase model performance?**

The original Starter_Code.ipynb has the basic neural network where there are 43 input variables. There are 2 hidden layers and both have 86 neurons. The general rule of thumb states to have 2-3 times the neurons as the input variable. Also the activation function used was relu in the 1st and 2nd hidden layer and Sigmoid in the output layer with 1 neuron. The total number of epochs are 50. The accuracy for this model is 0.728 which is less than the required optimization.

To get the desired optimization, I have made changes in the model layers and number if neurons and also reduced the input variable. 

In the second attempt as in the AlphabetSoupCharity.ipynb there are 43 input variables but the 1st layer has 129 neurons and relu activation function, the 2nd hidden layer has 129 neurons as sigmoid activation function, 3rd hidden layer has 86 neurons and sigmoid activation function and the output layer has the 1 neuron and sigmoid activation function. The number of epochs used to train the model is 100. The accuracy for this model is still 0.728 which is like the previous model.

In the next model in the AlphabetSoupCharity_Optimization.ipynb there are 42 input variables where the column of STATUS was additionally dropped. The cutoff for the classification was reduced to 1000. In this model there are 3 hidden layers where 1 layer has 111 neurons and relu activation function, 2nd layer has 74 neurons and relu activation function and 3rd hidden layer has 37 neurons and Sigmoid activation function. The last model is also trained on 100 epochs. Even though there have been some reduction in the input variables and the number of hidden layers and the neurons, the accuracy of the model did not change much. The accuracy remained almost the same at 0.728 which was close to the required model performance if not the same at 0.75. 

**Summary:**
There is a chance that if original data which was used to study is modified or more factors which have higher influence on the output result are chosen then there could be improvement seen in the model performance. There is also a possibility that if the model is trained on higher number of epochs it can yield better result.

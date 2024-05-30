# deep-learning-challenge
Links to Google Colab Notebooks: 
* Starter Code: https://colab.research.google.com/drive/1zQi_TIHk4rnBTfmakr_8Tp49e4QvMn-E?usp=sharing
* Optimized: https://colab.research.google.com/drive/13eVwcM40LLY71Mj3N1sWU051HOpcfH31?usp=sharing

## Written Report on Neural Network Model
#### Overview of the Analysis: 
The aim of this analysis is to assist the nonprofit organization Alphabet Soup in identifying potential funding recipients most likely to succeed. Utilizing the features within the dataset provided, I will develop a binary classifier capable of predicting the likelihood of success for applicants funded by Alphabet Soup.

From Alphabet Soup's business team, a CSV file has been provided containing data on over 34,000 organizations that have previously received funding. This dataset includes various columns capturing metadata about each organization, including:

  * **EIN** and **NAME**—Identification columns

  * **APPLICATION_TYPE**—Alphabet Soup application type
 
  * **AFFILIATION**—Affiliated sector of industry

  * **CLASSIFICATION**—Government organization classification

  * **USE_CASE**—Use case for funding

  * **ORGANIZATION**—Organization type

  * **STATUS**—Active status

  * **INCOME_AMT**—Income classification

  * **SPECIAL_CONSIDERATIONS**—Special considerations for application

  * **ASK_AMT**—Funding amount requested

  * **IS_SUCCESSFUL**—Was the money used effectively

#### Results: 
 **Data Preprocessing**
   1. What variable(s) are the target(s) for your model?

   * The target variable for the model is the 'IS_SUCCESSFUL' column because the goal is to identify applicants with the highest probability of success. This variable serves as a classification of the binary outcome, indicating success in charity donations or the effective utilization of funds.

   2. What variable(s) are the features for your model?

   * The variables that are features in the model are all columns excluding 'IS_SUCCESSFUL', which are:

  * **EIN** and **NAME**—Identification columns

  * **APPLICATION_TYPE**—Alphabet Soup application type
 
  * **AFFILIATION**—Affiliated sector of industry

  * **CLASSIFICATION**—Government organization classification

  * **USE_CASE**—Use case for funding

  * **ORGANIZATION**—Organization type

  * **STATUS**—Active status

  * **INCOME_AMT**—Income classification

  * **SPECIAL_CONSIDERATIONS**—Special considerations for application

  * **ASK_AMT**—Funding amount requested

  3. What variable(s) should be removed from the input data because they are neither targets nor features?

   * The variables `EIN` and `NAME` were removed from the input data becuase they are not relevant features of the analysis.
     
**Compiling, Training, and Evaluating the Model**
 1. How many neurons, layers, and activation functions did you select for your neural network model, and why?
    
    * For the optimized neural network model I selected three hidden layers with neuron amounts of 20, 25, and 5. Initally, in the starter code I tested 2 hidden layers with neuron amounts 95, and 30, which produced an accuracy score of .7299 (roughly 73%), realtively close to the target of 75% or higher. I used TensorFlow to test different different layers and neuron combinations and ran the model multiple times, changing the neruon amounts in increments of 10 and 5. Eventually the neuron amounts 20, 25, and 5 produced an accuracy score of 0.7305, which was slightly higher. Although it is not greater than 75%, this was the closest I could get it after running numerous trials. For the first two hidden layers I used the activation function ReLu to improve performance and explore non-linearity. For the third hidden layer, I used sigmoid because it is the most appropriate for binary classification tasks. For the output layer I also used the sigmoid activation function because I needed the output to fall between 0 and 1.

 2. Were you able to achieve the target model performance?

    * I was only able to acheive an accuracy score of around 73%, which falls just short of the target accuracy score of 75%.

 3. What steps did you take in your attempts to increase model performance?

    * I started by dropping the 'EIN' and 'NAME' columns to eliminate variables that could decrease accuracy. I also selected a cutoff value and generated a list of application types to be replaced (application_types_to_replace). This approach ensured that any application type with fewer than 500 occurrences is replaced with "Other". Similarly, a cutoff value was determined for the CLASSIFICATION column, and any classification with fewer than 1000 occurrences was replaced with "Other".
  
**Summary**

 * The deep learning model was able to achieve an accuracy score of 73% in classifying successful organizations based on their features. To optimize the model, several columns were dropped, categorical variables underwent a binning process, and hidden layers and neuron amounts were adjusted with each trial to improve accuracy. Looking at potential different learning models, ensemble methods like Random Forest or Gradient Boosting could be more advantageous for this analysis compared to neural networks due to their robustness to overfitting, inherent feature importance analysis, ability to handle non-linear relationships, ease of interpretation, and efficient performance on diverse datasets.

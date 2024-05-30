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

   * The variables that are features in the model are all columns excluding `IS_SUCCESSFUL`, which are:

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



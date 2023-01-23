# Neural Network Charity Analysis
## Overview of the analysis: 
  In this analysis, we are tasked with creating a binary classifier, neural network, which is capable of predicting whether applicants will be successful if funded by Alphabet Soup, a company which raises money to invest and fund foundations that are aim to improve the world. They have provided us with a CSV containing more than 34,000 organizations that have received funding from Alphabet Soup over the years. The csv file contains the following variables:
- **EIN** and **NAME**—Identification columns
- **APPLICATION_TYPE**—Alphabet Soup application type
- **AFFILIATION**—Affiliated sector of industry
- **CLASSIFICATION**—Government organization classification
- **USE_CASE**—Use case for funding
- **ORGANIZATION**—Organization type
- **STATUS**—Active status
- **INCOME_AMT**—Income classification
- **SPECIAL_CONSIDERATIONS**—Special consideration for application
- **ASK_AMT**—Funding amount requested
- **IS_SUCCESSFUL**—Was the money used effectively</br></br>

### Steps to Complettion
Deliverable 1: Preprocessing Data for a Neural Network Model</br>
Deliverable 2: Compile, Train, and Evaluate the Model</br>
Deliverable 3: Optimize the Model</br>


## Results: 
### Data Preprocessing
- What variable(s) are considered the target(s) for your model? IS_SUCCESSFUL
- What variable(s) are considered to be the features for your model? APPLICATION_TYPE, AFFILIATION, CLASSIFICATION, USE_CASE, ORGANIZATION, STATUS, INCOME_AMT, SPECIAL_CONSIDERATIONS, and ASK_AMT
- What variable(s) are neither targets nor features, and should be removed from the input data? EIN and NAME
### Compiling, Training, and Evaluating the Model
- First Model
![image](images/model_1.png)
  - neurons:  80-30
  - layers: 2 hidden; 1 output
  - activation functions: relu and sigmoid
![image](images/model_1_results.png)
  - the model did not hit the required performance accuracy level, only accomplishing 72.5%

- Second Model: Binning/OneHotEncoding the ASK_AMT and Increasing Neurons
![image](images/modle_2_binning.png)
![image](images/model_2.png)
  - neurons:  100-50
  - layers: 2 hidden; 1 output
  - activation functions: relu and sigmoid
![image](images/model_2_results.png)
  - the model did not hit the required performance accuracy level, only accomplishing 73% (improved accuracy by about 0.5%)
- Third Model: Adding a Third Hidden Layer
![image](images/model_3.png)
  - neurons:  100-50-30
  - layers: 3 hidden; 1 output
  - activation functions: relu and sigmoid
![image](images/model_3_results.png)
  - the model did not hit the required performance accuracy level, only accomplishing 72.9% (no real improvement)</br></br>

## Summary: 
Overall, there is still a need to improve the neural netowrk model for Alphabet Soup. One recommendation is to try different activation functions in the hidden layers, increse epochs from 100 to 200, and look into the data variables STATUS and SPECIAL_CONSIDERATIONs to see if they can be removed.

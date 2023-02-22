Alphabet Soup Charity

Overview of the analysis: 
The nonprofit foundation Alphabet Soup has requested a tool that can assist in the selection of applicants for funding. The requirement is for the model to identify candidates with the best chance of success in their ventures. 

Alphabet Soup’s business team provided a data set that contained 34,000 organizations that have received funding from Alphabet Soup over the years. Within this dataset were several columns that capture metadata about each organization. An explanation of the data and there definitions are provided below. 

Data 
EIN and NAME—Identification columns
APPLICATION_TYPE—Alphabet Soup application type
AFFILIATION—Affiliated sector of industry
CLASSIFICATION—Government organization classification
USE_CASE—Use case for funding.
ORGANIZATION—Organization type
STATUS—Active status
INCOME_AMT—Income classification
SPECIAL_CONSIDERATIONS—Special considerations for application
ASK_AMT—Funding amount requested
IS_SUCCESSFUL—Was the money used effectively

Data Preprocessing

EIN and Special_Considerations were dropped from the model all other variables were used. 
NAME—Identification columns
APPLICATION_TYPE—Alphabet Soup application type
AFFILIATION—Affiliated sector of industry
CLASSIFICATION—Government organization classification
USE_CASE—Use case for funding
ORGANIZATION—Organization type
STATUS—Active status
INCOME_AMT—Income classification
ASK_AMT—Funding amount requested
IS_SUCCESSFUL—Was the money used effectively
These data elements appeared to provide the most infomration for the model.

Is Successful is the features for this model because it identifies whether money issued was used successfully or not.

EIN and Special_Considerations were removed from the input data because they are neither targets nor features?

How many neurons, layers, and activation functions did you select for your neural network model, and why?
The neural network model created, contains two hidden layers with 8 and 6 nodes respectively. The original model run ressulted in 73% accuracy. Once Name was added and Special_Considerations was removed from the model, accuracy went up to 75%. Adding name back to the model and creating bins added details to the model that improved acuaracy.

After reviewing each of the data inputs, it was determined that associating the name of the company with the rest of the data helped improve the model accuracy. Also, Special_Considerations only had 2 unique value counts which didn't provide much useful information. Taking Special_Considerations and incorporating Name improved model accuracy. 

Summary: After procesing the data and updating the categories to be used, the nueral netwrok model accuracy was 75% which is a good tool to allow Alphabet Soup Charity identify good candiates for funds. While I was able to build a neural network that is dependable, I believe since we are trying to classify something as good candidate or bad, a supervised learning classification model (logistics regression) could have been used to provide the same if not better result. In addition, the supervised technique is a little eaiser to explain to a customer. 

Files:
StarterCode - Initial data processing and model development 
AlphabetSoupCharity.h5 - Saved model output 
charity_data.csv - Data file 
AlphabetSoupCharity_Optimization.ipynb - Optimized model 
AlphabetSoupCharity_Optimization.h5 - Saved model 
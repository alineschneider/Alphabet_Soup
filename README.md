# Alphabet_Soup

## Project Description
The project consisted of creating a machine learning model to predict the success of a venture paid by Alphabet Soup.

## Resources
- Data source:
    - charity_data.csv
- Software: Python 3.7.7, Jupyter Notebook, Visual Studio Code 1.43.1

## Preprocessing
* Dropped identification column (EIN). Each number appears only once in the dataset.
* Bucket NAME (frequency less than 10 = 'Other')
* Bucket APPLICATION_TYPE (frequency less than 100 = 'Other')
* Target variable: IS_SUCCESSFUL

## Model Optimization
__1.__ Number of neurons and layers selected for neural network model:\
Single layer with twice as many neurons as the number of input features. 

__2.__ Steps taken to try and increase model performance:
* Made sure to not bucket together too many of the rare categorical values when preprocessing so as not to lose too much data; 
* Increasing the number of neurons to 3x the number of input features did not improve accuracy significantly;
* Running more epochs (150) improved accuracy slightly, but not enough to justify the additional epochs;
* Creating a Deep Learning model by adding a second layer with 10 neurons resulted in the model overfitting the training data. Reducing the epochs to 50 and changing the number of neurons in the hidden layers to 30 and 10 did not improve it.

__3.__ Different model that could be implemented to solve this classification problem:\
Support Vector Machine - SVM. They are very effective in classifying and creating regression using two groups, which was the nature of the current project: binary classification.

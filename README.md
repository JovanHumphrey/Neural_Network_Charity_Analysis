# Neural_Network_Charity_Analysis #

## Project Overview ##

<p>The purpose of this project was to help the charity Alphabet Soup determine which companies are good investments. Because we didn't know what shape the final result would take, I chose to use a neural network to train and test the data.</p>

<p>Preprocessing the data required dropping unused columns and determining the unique values in each column. For columns APPLICATION_TYPE and CLASSIFICATION I created density-plots to determine the distribution of the column values. </p>

<p>Next I determined that the values in column IS_SUCCESSFUL should be the target data, and that data in columns APPLICATION_TYPE, AFFILIATION, CLASSIFICATION, USE_CASE, ORGANIZATION, INCOME_AMT, and SPECIAL_CONSIDERATIONS would be the model's features.</p>

## Data Processing ##
### Compiling Data and Evaluating the Model ###
<p>Initially I compiled the data using the following parameters:</p>

<p>• 2 hidden layers</p>
<p>• layer 1: 80 neurons; activation="relu"</p>
<p>• layer 2:  30 neurons; activation="relu"</p>
<p>• Trained with 30 epochs</p>
<p><b>• Result: 72.6% accuracy</b></p>

<p>Because the results were less than 75% accuracy, I tested the model again three more times making adjustments to each one.</p>

### Attempt 1 ###
<p>• 3 hidden layers</p>
<p>• layer 3: 15 neurons; activation="relu"</p>
<p>• Trained with 50 epochs</p>
<p><b>• Result: 72.5% accuracy</b></p>

<p>For attempt 1 I thought that perhaps an additional hidden layer and additional epochs might improve accuracy. The accuracy decreased marginally.</p>

### Attempt 2 ###
<p>• 3 hidden layers</p>
<p>• layer 1: 100 neurons; activation="tanh"</p>
<p>• layer 2: 50 neurons; activation="tanh"</p>
<p>• layer 3: 25 neurons; activation="tanh"</p>
<p>• Trained with 70 epochs</p>
<p><b>• Result: 72.3% accuracy</b></p>

<p>Still hoping my instincts were right, I kept the third hidden layer in attempt 2, increase the neurons in each layer, and increased the epochs yet again. This time I changed the activation function from relu to tanh, but the results were even worse than before.</p>

### Attempt 3 ###
<p>• Remove columns 'USE_CASE', 'SPECIAL_CONSIDERATIONS', and 'ASK_AMT'</p>
<p>• layer 1: 100 neurons; activation="relu"</p>
<p>• layer 2: 50 neurons; activation="relu"</p>
<p>• layer 3: 25 neurons; activation="relu"</p>
<p>• Trained with 100 epochs</p>
<p><b>• Result: 72.6% accuracy</b></p>

<p>For my final attempt I considered that perhaps there was too much noise in the data, so I dropped additional columns. I kept the third hidden layer and reverted the activation function back to relu. Once again I added more epochs. This performed better than my first attempt but only by a little. In the end none of these attempts got us to the target of 75%.</p>


## Summary ##

<p>After a total of 4 trials using deep-learning I wasn't able to reach the target of 75% accuracy. It's possible that my changes caused overfitting. Perhaps using a Random Forest Classifier could generate more accurate predictions. It may also require more data to develop a better performing model.</p>

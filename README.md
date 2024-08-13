# Module21
# Overview
This analysis is meant to develop a model for identifying applicants that would succeed if funded by Alphabet Soup.

# Results
- We are targeting the "IS_Successful" variable in our models
- Our features are the status, ask amount, application type, income amount, and special considerations flag
- we removed the EIN and Name variables from the model since they are neither features nor target variables
- In our initial efforts, we went with 3 layers, using 8, 5, & 1 neurons respectively. These were chosen based off of my experience in our lesson for building nn models
- Our initial accuracy was 0.7294, which was below target performance
- I tried editing the layer neuron counts, epoch count, and activation method for optimizing the model, as I felt more comfortable editing those factors over changing our preprocessing methods and data manipulation. I found that decreasing the neurons in the first hidden layer increased accuracy, but changing any neuron count in layer 2 had an adverse effect. I tried both raising and lowering the epoch count, and both tweaks lowered accuracy, so for the final model I kept the epoch count at 100. Finally, I tried a few different configurations of activation methods across the 3 layers, and saw a small improvement when I changed all activation methods to sigmoid over using relu in the two hidden layers.

# Summary
While the model has a decently high accuracy, it still does not meet performance goals. 
As opposed to a neural network, we could use a random forest model to solve this problem. I recommend this due to the high number of classification based features in this data set (use_case, affiliation, application_type, Organization, status, etc.). Decision trees can handle these types of data to build a model, and I would suggest attempting one to see if it would be more accurate than a neural network.

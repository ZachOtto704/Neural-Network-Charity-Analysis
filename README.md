# Neural-Network-Charity-Analysis

Overview of Analysis:

The purpose of this analysis was to help AlphabetSoup determine which donation recievers are likely to usefully or not usefully use donated funds. We created a neural network model to process AlphabetSoup donation data and predict whether a given company would usefully use donated funds. 


Results:

Below is the raw csv data we used:

![image](https://user-images.githubusercontent.com/112716673/214911803-b34318bf-3f1a-4d05-b24b-2ed04114baa1.png)

-The target variable for our model is "IS_SUCCESSFUL". This data is a binary output of whether the company recieving donations either sucessfully used their funds(1), or did not (0).

-The features we dropped from this data before running our model was "EIN" and "NAME". Although this data is useful to us as a reader, in identifying what company is related to the data, the neural network model will make nothing of it, and could interpret the EIN as numerical data instead of categorical. 

-The features we used in the initial model was every other column (besides our target, and dropped columns). 

-We used 2 hiden layers with 40 neurons and 20 neurons respectively. I started with fewer neurons and then added more in hopes of achieving higher accuracy. 

-I was not able to achieve target model performance. I reached 60%, 58%, and 56%. Moving in the wrong direction.

-In attempt to increase model performance, I first tried reprocessing the data. First I simply added more neurons to the hidden layers. This did not have much effect on the outcome accuracy. So I decided to try altering the preprocessed data. I felt what the application type data may have simply been an administrative formality and did not have an actual effect on the company's ability to successfully use funds. So I dropped these columns from the data being used in the model. After that, I also tried using a Leaky_relu activation function in the hidden layers instead of regular Relu. This combination created less accuracy then the initial model.


Summary: 

I was not able to achieve target model performance. I reached 60%, 58%, and 56%. Moving in the wrong direction. A take away here, is that the application type data that I thought was skewing the model, is actually probably useful for improving accuracy. And the relu activation in the hidden layers is better used than the leaky relu. I would consider adding more layers or neurons to the model, but that runs the risk of overfitting the model to this specific data. One way to perhaps improve the model's accuracy is to experiment with ensemble methods, such as combining a decision tree with the neural network model.


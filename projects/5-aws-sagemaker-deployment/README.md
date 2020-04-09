# SageMaker Deployment Project

The [notebook](SageMaker%20Project.ipynb) and Python files provided here, once completed, result in a simple web app which interacts with a deployed recurrent neural network performing sentiment analysis on movie reviews, telling if the review is positive or negative.

The cleaning process was to remove all the HTML tags with [BeautifulSoup](https://www.crummy.com/software/BeautifulSoup/bs4/doc/). Then we stemmed the word with the library [nltk](https://www.nltk.org/) so words like *entertained* and *entertaining* becomes the same *entertain*.

Then we did a dictionnary with the 5000 most common words in the reviews data set. This is the dictionnary the RNN would use to train on extracting the sentiment of the review.

Once we trained the model with SageMaker, we deploy it to create an accessible endpoint to that model.

The next step were to create an AWS Lambda function and an API Gateway. Basically, our simply web app would sent the form review text to the API Gateway, which would send the text to the lambda function. The lambda function job is to call the model endpoint with a review to make a prediction. Once the model returned a prediction to the lambda function, it returns it the API Gateway, which returns it back to the Web App front end that can display the result, positive or negative review.

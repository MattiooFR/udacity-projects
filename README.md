# Projects done during my Udacity Training

___

## [Bike Sharing Prediction](bike-rental-prediction/)

This is a **13 hidden node** that predict the rate of usage for bike sharing with a wide range of previous data input like bike sharing usage, temperature, weather, ...

**Learning rate** is 0.7 with 7000 iterations. The model obtain 6% mistake on the training set, and 15% mistake on untrained data.
The final delta of mistakes between training set and untrained data is because the used untrained data is during the month of december, and the model wasnt trained with enough christmas data to be efficient predicting data during that period.

___

## [Sentiment Analysis Network](sentiment-analysis-network/)

This project was about learning to clean the data and remove useless calculus of the algorithm to improve a neural network prediction for reviews about movies. At first, the model was able to get 70% success predicting if a review was positive or negative. It was trained by giving stronger weight to big count of words from each review.

The **first improvment** we did was to stop using the count of each word as most of the words were neutral like a, the, " ", ".". By doing this we improved the training up to 84% success of prediction.

The **next step** was to make the training much more faster by removing all unacessary calculus. We were using 70 000 inputs and most of the time doing vector multiplication by 0. By removing this part the training was going 8-9 times faster.

The **last step** was to clean the data and remove the most common words that were neutral and keeping the less used words but that had a stronger impact on determining if a review was positive or negative. This was also making the training and testing faster as the amount of inputs words drastically reduced.

With all this, we managed to train our network faster by a factor of 50x, and keeping the accuracy around **80-85%**.

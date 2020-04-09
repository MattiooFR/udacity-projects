[//]: # (Image References)

[image1]: ./images/sample_dog_output.png "Sample Output"

## Project Overview

Welcome to the Convolutional Neural Networks (CNN) project in the AI Nanodegree! Given an image of a dog, the algorithm can identify an estimate of the canine’s breed. If supplied an image of a human, the code will identify the resembling dog breed.

I first used PyTorch to create a CNN and trained it on the dog data set to realise that the task was quite hard.

Then I used transfert learning to get better result. I used a pretrained densenet121 on ImageNet, and I changed the classifier to be connected to 133 outputs instead of 1024. Those 133 outputs represents the different dog breeds. Doing so I achieved 85% accuracy.

The whole notebook can be found [here](dog_app.ipynb)

![Sample Output][image1]

## Project Instructions

### Instructions

1. Clone the repository and navigate to the downloaded folder.
2. Download the [dog dataset](https://s3-us-west-1.amazonaws.com/udacity-aind/dog-project/dogImages.zip).  Unzip the folder and place it in the repo, at location `path/to/dog-project/dogImages`.  The `dogImages/` folder should contain 133 folders, each corresponding to a different dog breed.
3. Download the [human dataset](http://vis-www.cs.umass.edu/lfw/lfw.tgz).  Unzip the folder and place it in the repo, at location `path/to/dog-project/lfw`.  If you are using a Windows machine, you are encouraged to use [7zip](http://www.7-zip.org/) to extract the folder.
4. Make sure you have already installed the necessary Python packages according to the README in the program repository.
5. Open a terminal window and navigate to the project folder. Open the notebook and follow the instructions.

```bash
jupyter notebook dog_app.ipynb
```

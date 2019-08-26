# Ex2: Introduction to Azure ML Studio

The sinking of the RMS Titanic is one of the most infamous shipwrecks in history.  On April 15, 1912, during her maiden voyage, the Titanic sank after colliding with an iceberg, killing 1502 out of 2224 passengers and crew. This sensational tragedy shocked the international community and led to better safety regulations for ships.

One of the reasons that the shipwreck led to such loss of life was that there were not enough lifeboats for the passengers and crew. Although there was some element of luck involved in surviving the sinking, some groups of people were more likely to survive than others, such as women, children, and the upper-class.

In this challenge, we ask you to complete the analysis of what sorts of people were likely to survive. In particular, we ask you to apply the tools of machine learning to predict which passengers survived the tragedy.

    Binary classification
    Multi class classification
    Python and R basics
    
### Variable Notes

**class**: A proxy for socioeconomic status (SES)
1st = Upper
2nd = Middle
3rd = Lower

**age:** Age is fractional if less than 1. If the age is estimated, is it in the form of xx.5

**sibsp**: The dataset defines family relations in this way...
Sibling = brother, sister, stepbrother, stepsister
Spouse = husband, wife (mistresses and fiancés were ignored)

**parch**: The dataset defines family relations in this way...
Parent = mother, father
Child = daughter, son, stepdaughter, stepson
Some children travelled only with a nanny, therefore parch=0 for them.


## Step #1 : Load Dataset
Log in Azure-ML account then go to Dataset and click on new, browse your dataset file and upload our Excel or CSV file. We are going to use this dataset as a training model

![](https://raw.githubusercontent.com/lcarcamo1526/ML-Exercises/master/Ex2/Img/1.gif)

## Step #2 : Features

We need choose our features and manipulate our data, so we're going to add a **Project Columns** component to choose the features to train our model. 
The columns that we're going use are : ***Sex, Age, Class, Fare, Survived***

![](https://raw.githubusercontent.com/lcarcamo1526/ML-Exercises/master/Ex2/Img/2.gif)

## Step #3 : Clean Data

As in most cases we sometimes deal with data that are missing information, in this case we know that not all entries contain the age of the person, we will replace those entries with the median of the entire population.

![](https://raw.githubusercontent.com/lcarcamo1526/ML-Exercises/master/Ex2/Img/3.gif)

## Step #4 : Split Data and Train Model

After confirm the relation between these variables we need split data for training and testing purpose. In the left bar we search for "split data" and drag and drop to main window, then click on the previous node and drag a relation to Split data, finally we divide the data into 3/4 (Training) and 1/4 (Testing)

After split our data, we need train our model, in this case we're going use a Multi class Forest Algorithm
In the left bar add Train model component and then add Multi class Forest

![](https://raw.githubusercontent.com/lcarcamo1526/ML-Exercises/master/Ex2/Img/4.gif)


## Step #5 : Choose label data

Before train our model, we need choose our label data, this labeled data is going to be our prediction, in our case is going to be the ***Survived*** Column, also we need be sure about our training rate and our test rate.


![](https://raw.githubusercontent.com/lcarcamo1526/ML-Exercises/master/Ex2/Img/5.gif)

## Step #6 : Score our model

After did all previous step, we need check the performance of our model, for this step we are going to use the Score Model component and Evaluator component, this last one is going to compare using MSE to check How far is our prediction of the train values 


![](https://raw.githubusercontent.com/lcarcamo1526/ML-Exercises/master/Ex2/Img/6.gif)

## Step #7: See results:

Finally, after train and test our model, we're going to look how well is running our model, for this press right click on the model Evaluator component, and then press Visualize.

![](https://raw.githubusercontent.com/lcarcamo1526/ML-Exercises/master/Ex2/Img/7.png)


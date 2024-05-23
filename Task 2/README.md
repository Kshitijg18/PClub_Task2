
# Link to Google drive for dataset
https://drive.google.com/drive/folders/1UzHFWEfFjSFQ2ig1lGUSFDkXscpzi-da?usp=sharing

I have also uploaded dataset on Github Repo
# Approach for Dataset

For the dataset I started by searching datasets directly for Tidal Volume and had no luck in finding it. Later I surfed a bit to get to know when someone gets his tidal volume measured. For that I found a list of diseases. Although, the exact name of disease didn't help that much. But I found I dataset on kaggle named Lung_Disease that had FVC in in. On internet I found FVC/10 is approx equal Tidal Volume. I had one in hand still I searched for another. I got another on Kaggle but the dataset felt fake as it had senseless values like a 6 year child standing more than 5 feet. There were many such instances hence I dropped the idea of using it even though it had more entries then my previous dataset.

# Approach for Problem
My dataset had many biological parameters measured. So when I used linear regression the mean square error was very large as they are not linearly dependent. Then I decided to make a neural network for training.

### How I increased the accuracy
- I started with a simple 3 dense layer model (1 hidden layer). Still it had error quite big. 
- Then I thought of droping some of the parameters and it rather increased the error. So I tried different number of layers and 2 hidden layers worked well. Still the accuracy was not good.
- I increased number of neurons in each layer and it helped. I started with 100 epochs increased it. Also I tried reducing learning rate and increasing epochs. At last I chose the combination that I felt was working the best. Higher then 250 epochs was causing overfitting.
- To suffice with the dataset I had, I split in 9:1 train test ratio. Also while training I kept validation split to 0.1. Both of these helped in increasing the accuracy 

# How to run model
First ensure downloading all the files including the model named 'Tidal_Volume(litre).keras' and keep them in the same directory. Then You can run the first and last cell of 'Model.ipynb'. There you will get the dataframe comparing actual and predicted tidal volume. It will also print the mean square error. If you want to check on your own data. I have made a file 'Load_in_it.ipynb'. Please add the testing file in the same format as my dataset and run the file as intructed in the code.

# Screenshots of Model in action

[![Screenshot-2024-05-23-at-4-45-16-PM.png](https://i.postimg.cc/vmwQbYc8/Screenshot-2024-05-23-at-4-45-16-PM.png)](https://postimg.cc/VJ4yFcq2)


[![Screenshot-2024-05-23-at-4-48-50-PM.png](https://i.postimg.cc/1tJPGDM4/Screenshot-2024-05-23-at-4-48-50-PM.png)](https://postimg.cc/7GGpDGFy)

[![Screenshot-2024-05-23-at-4-50-22-PM.png](https://i.postimg.cc/d1qwZ52z/Screenshot-2024-05-23-at-4-50-22-PM.png)](https://postimg.cc/Ffn22gnZ)
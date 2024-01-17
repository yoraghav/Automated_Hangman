# Automated_Hangman

The project provides automated guesses of the letters in the game of hangman. The repository contains 3 notebooks -  one for data creation, one for model training and one for model testing and actual game playing. You can either train your own model on your own dictionary of words named "dictionary.csv" OR download my trained CatBoost model at https://shorturl.at/ejDNV

The working and logic behind the solution is provided in the link containing the model itself.

## PERFORMANCE 

The entire model structure combined with two algorithms gives a pretty good accuracy overall. With 6 number of max wrong guesses the model performs with 95% accuracy on the words in the training dictionary of the model and 67% accuracy on unseen words from out of the dictionary.

## DATASET CREATION 

Replace the name "words_250000_train.txt" in the ipynb and perform full creation of the dataset. The code utilises multicore processing on your device for faster processing. The size magnification is huge though so keep in mind the words you want to train your model on. For e.g. the dataset I created used 250k words and the size of the embedding dataset was around 1.5GB in .csv and 400 MB in .parquet.

## MODEL TRAINING 

Replace the "fd.parquet" with your own output dataset from the dataset_creation file and then train the model. The model uses 26 classification models for better performance and might take a while.

## MODEL TESTING

You can import your own model or import my already trained model in the above mentioned link. There are 2 modes of testing - one where with verbose = True and the model will output each iteration of the guess for the word and you can use this to analyze the pattern of your model. In second you can specify the max number of guesses for the game and check the overall accuracy of the model by randomly selecting words from the dataset you provide. 

Enjoy!

# Text-Prediction

This text prediction model implements a statistical trigram language model with NLTK for text prediction based on the Alice(alice.txt file) in Wonderland corpus.
An n-gram language model is a language model that models sequences of words as a Markov process. It makes use of the simplifying assumption that the probability of the next word in a sequence depends only on a fixed size window of previous words. A trigram model considers two previous words , thats why in this model we input a phrase of 4 letter words for predictions. 

## Getting started

1. clone or download this repository in your prefered notebook e.g colab
```sh
!git clone https://github.com/ganyiwatakunda/Text-Prediction.git
```
2. run main.py
```sh
!python main.py
```
5. once prompted by the program, enter a 4 letterd phrase related to the Alice corpus

## Demo

Here is an example of the program output:
![demo image of running program](https://github.com/ganyiwatakunda/Text-Prediction/blob/master/images/TextPredictionSample.png)
### final output of demo:
User input: ***i wish you were*** <br />
Prediction: ***i wish you were all talking together***<br />
Who was Alice wishing they were all talking together ?? The suspense...😖 <br />

## Implementation
I used NLTK's probability library to store the probability of each predicted word,
```sh
ConditionalFreqDist()
```
then the program picks from a weighted random probability to decide which prediction to append to the given phrase.
```sh
random.choices()
```
The user decides when to stop the program by choosing whether or not to predict the next word.
```sh
"Do you want to generate another word? (type 'y' for yes or 'n' for no): "
```

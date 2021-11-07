# Testing STT performance on DC-TTS - _A Tensorflow Implementation of DC-TTS_.  

## Requirements:

* NumPy >= 1.11.1
* TensorFlow >= 1.3
* Librosa
* tqdm
* matplotlib
* scipy

## Data

The original repository provides us with a [pre-trained model](https://www.dropbox.com/s/1oyipstjxh2n5wo/LJ_logdir.tar?dl=0) based on the LJ Speech Dataset. With that, we are able to test the performance of the TTS model with pre-defined or custom sentences (see further steps).


## Original repository

The [original implementation](https://github.com/Kyubyong/dc_tts) makes use of a technique based on Convolutional Neural Networks (cnn) discussed in [this article](https://arxiv.org/abs/1710.08969). This is preferred to techniques involving Recurrent Neural Networks (RNN), because CNN-based synthesis requires less computing power and can be done faster. In this original repository a STT model was trained with the LJ dataset we are using, but also for Kate Winslett's and Nick Offerman's voices and even for a Korean speaker. The TTS model was originally tested with the [Harvard sentences](http://www.cs.columbia.edu/~hgs/audio/harvard.html) which are recommended sentences to test TTS applications.

## The task

For our task we did not just want to replicate the original results by using the pre-defined sentences that are synthesized, but we also wanted to be able to dynamically run inference on the Text-to-Speech model. This means that, besides replicating the previous synthesis, we wanted to be able to either use the examples from the Harvard sentences or to use our own sentences to synthesize. In terms of results, we expect the TTS synthesizer to be able to work with any input from the English language.

## How does the code work?

Here, you have two choices: 
 * Simply press  [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1lg4HmCD_GhuoJjLPpfel0npiw5FxBQxk?authuser=1#scrollTo=ZNFKOgHQOtGL)  to open our Google Colab notebook. 
 * Or: download the [DC_TTS_test.ipynb](https://github.com/jkuhlemann/dc_tts/blob/test_inference/DC_TTS_test.ipynb) to your computer and then open it in a Google Colaboratory environment and follow each step. 

The Python notebook should be self-explanatory and easy to follow. Basically, it follows these steps in order to test the TTS model:

  * STEP1: Clone the repository
  * STEP2: Create necessary folders
  * STEP3: Download & extract the pre-trained model
  * STEP4: Customize sentences to be used for TTS synthesis or stick with pre-defined ones
  * STEP5: Synthesize the sentences and play the desired audio-file

## Results

The code is working as it is supposed to. It automatically plays a .wav file that corresponds to the choice of the user. One challenge we encountered was having to change lines in hyperparams.py in order to load the right directories, since the code was most likely not intended to run in a Google Colab environment. The model dealt well with general English input, but struggled with foreign words and (proper) names. For example, the TTS model is barely able to produce a proper pronunciation of a typical Dutch name like Wouter. We did expect this to occur though, because the model is specifically trained with English language data.

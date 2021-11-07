# Text-to-speech model: A TensorFlow Implementation of DC-TTS.



## Requirements:

* NumPy >= 1.11.1
* TensorFlow >= 1.3
* Librosa
* tqdm
* matplotlib
* scripy

## Data

For the data set, we've used the [LJ Speech Dataset] (https://keithito.com/LJ-Speech-Dataset/), which is a widely used dataset in Text-to-Speech due to it being publicly available, with 24 hours of samples. We are also using [Harvard sentences] (http://www.cs.columbia.edu/~hgs/audio/harvard.html) as text input.

## Original repository

The [original repository] (https://github.com/Kyubyong/dc_tts) is based on [this article] (https://arxiv.org/abs/1710.08969) which makes use of a technique based on Convolutional Neural Networks (cnn). This is preferred to techniques involving Recurrent Neural Networks (RNN), because CNN-based synthesis requires less computing power and can be done faster. In this original  repository a synthetic voice was made with the LJ dataset we are using, but also for Kate Winslett's and Nick Offerman's voice and even for a korean speaker. [Harvard sentences] (http://www.cs.columbia.edu/~hgs/audio/harvard.html) were used as text input, so the synthesized voice also uses these phrases as output.

## The task

Our task is not just about replicating the original repository by using the LJ Speech Dataset, we also wanted to be able to customize the Text-to-Speech input. This means that we want to offer the choice to users to either use random examples from the Harvard sentences or to use their own sentences to synthesize. In terms of results, we expect the TTS synthesizer to be able to work with any input from the English language.

## How does the code work?

STEP1: Clone the repository

STEP2: Create necessary folders

STEP3: Download & extract the pre-trained model

STEP4: Create a function to customize sentences to be used for TTS

STEP5: Synthesize the sentences and play the desired audio-file

## Results

The code is working as it is supposed to. It automatically plays a .wav file that corresponds to the choice of the user. One challenge we encountered was having to change lines in hyperparams.py in order to load the right directories. Another challenge is the pronunciation of non-English words, as the TTS synthesizer is barely able to pronounce a typically Dutch name like Wouter. We did expect this to occur though, because the model is specifically trained with the English language.




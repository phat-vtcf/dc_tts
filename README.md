## Requirements
  * NumPy >= 1.11.1
  * TensorFlow >= 1.3 (Note that the API of `tf.contrib.layers.layer_norm` has changed since 1.3)
  * librosa
  * tqdm
  * matplotlib
  * scipy
  
## Data
we are using a pretrained model from https://github.com/Kyubyong/dc_tts , which is trained by LJ Speech Dataset. The seven wav files in samples folder are the synthesized audio.

## Pretrained Model for LJ

Download [this](https://www.dropbox.com/s/1oyipstjxh2n5wo/LJ_logdir.tar?dl=0).

## Synthesis
We generate speech samples based on our programing course description. Its txt file is included in the repo.
  * Download the pretrained model and unzip it. Then create a new folder named "logdir" in the directory, and put the two model folders inside of it. The folder belongs in the same directory as the repository

  * Run `synthesize.py` and check the files in `samples` 

## Notes
   * To run the repo locally, python version lower than 3.7 is required for instaliing tensorflow 1 on your computer
   * You need to used the code in script2run.py in your IDE in script mode to synthesize.
   * The first line of the txt file will be skipped, so better leave the start of your text to the second line

## Findings
   * There is a character number limit for one sentence, otherwise it will have error message and we need to split it into different audio files, which the author didn't mention it. 
   * Sometimes there is high frequency noise when binding the syllables together.
   * Some sentences sound cut off in the end as if the last phoneme is missing.

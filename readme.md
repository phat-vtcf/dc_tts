## Requirements
  * NumPy >= 1.11.1
  * TensorFlow >= 1.3 (Note that the code doesn't work for tensorflow 2)
  * librosa
  * tqdm
  * matplotlib
  * scipy

## Model
we used a pretrained model from https://github.com/Kyubyong/dc_tts. The download link of the model is https://www.dropbox.com/s/1oyipstjxh2n5wo/LJ_logdir.tar?dl=0

##  Synthesis
we used the text from programming course description. It is already included in the repo.

  * Run `synthesize.py` and check the files in `samples`.
##  Note
to run this repo locally, please make sure you are using tensorflow 1. To install it, you need python version lower than 3.7

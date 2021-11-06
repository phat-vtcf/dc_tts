## Requirements
  * NumPy >= 1.11.1
  * TensorFlow >= 1.3 (Note that the code doesn't work for tensorflow 2)
  * librosa
  * tqdm
  * matplotlib
  * scipy

## Data

we used a pretrained model from https://github.com/Kyubyong/dc_tts. The model is trained by LJ Speech Dataset. Click the original repo for more details.

## Sample Synthesis
We generate speech samples based on the course description of our programing course . It is already included in the repo. The file name is programming_course_description.txt

  * Run `synthesize.py` and check the files in `samples`.The corresponding 7 wav files are the generated synthesized audio.

## Pretrained Model

You can Download the model from here [this](https://www.dropbox.com/s/1oyipstjxh2n5wo/LJ_logdir.tar?dl=0).

## Notes
   * To run this repo locally, please make sure you are using tensorflow 1. To install it, you need python version lower than 3.7
   * You need to type the code in script2run.py in the ide in script mode to generate audio

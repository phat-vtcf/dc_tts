The purpose of this repo is to replicate TTS training as presented in the repository 
dc_tts

The steps needed to run it are the following:

0. If you downloaded the synthesize.ipynb file skip to step 5, else:

1. clone the git

2. cd into the git

3. paste the code from synthesize.py in a Google Colab Notebook 

4. get the right version of tensorflow by pasting the following code on top of the document:
%tensorflow_version 1.x

5. download the LJ_logdir.tar file from here: https://www.dropbox.com/s/1oyipstjxh2n5wo/LJ_logdir.tar?dl=0

6. unzip the LJ_logdir.tar file and save the content in a folder called logdir

7. upload the logdir folder to your Google Drive

8. replace the path in the Google Colab Notebook created in step 3 in:
   saver1.restore(sess, tf.train.latest_checkpoint("PLACE PATH HERE/logdir/LJ01-1"))

   and also in:
   saver2.restore(sess, tf.train.latest_checkpoint("PLACE PATH HERE/logdir/LJ01-2"))
  
9. Run the Google Colab Notebook

10. The resulting files will be saved as .wav files in the samples folder

If you want to run the code again, make sure to restart the runtime, because Google Colab does not
remember which version of tensorflow it was running

The purpose of this repository is to easily replicate TTS synthesis as presented in the repository: dc_tts

In doing so we used the provided pretrained model which you can download here: https://www.dropbox.com/s/1oyipstjxh2n5wo/LJ_logdir.tar?dl=0

The original repository can be accessed via: https://github.com/Kyubyong/dc_tts

The text-to-speech model used in this repository has been introduced in: https://arxiv.org/abs/1710.08969

The repository uses the first list of Harvard sentences to test the speech quality of the text-to-speech model.
This list can be found on: http://www.cs.columbia.edu/~hgs/audio/harvard.html

------------------------------------------------------------------------------------------------------------------------------------
The steps needed to run the synthesis process using the pretrained model are the following:

0. Make sure the following libraries are installed, you can do this by using the 'pip install' command from the (Anaconda) command prompt.
- NumPy >= 1.11.1
- TensorFlow >= 1.3
- librosa
- tqdm
- matplotlib
- scipy

1. If you downloaded the synthesize.ipynb file skip to step 7, else:

2. clone the git

3. change the directory to the git repository by using the 'cd' command, combined with the name of the repository.

4. open the synthesize.py file by using the 'cat synthesize.py' command.

5. copy the code and paste it in a Google Colab Notebook 

6. get the right version of tensorflow by pasting the following code on top of the document in a/the code block*:
%tensorflow_version 1.x

7. If you haven't done so yet, download the LJ_logdir.tar file from here: https://www.dropbox.com/s/1oyipstjxh2n5wo/LJ_logdir.tar?dl=0

8. unzip the LJ_logdir.tar file and save the content in a folder called logdir

9. upload the logdir folder to your Google Drive

10. replace the path in the Google Colab Notebook we provided (synthesize.ipynb) or in the Google Colab Notebook that you created in step 5 in: 

saver1.restore(sess, tf.train.latest_checkpoint("PLACE PATH HERE/logdir/LJ01-1"))

and also in: 

saver2.restore(sess, tf.train.latest_checkpoint("PLACE PATH HERE/logdir/LJ01-2"))
  
11. Run the Google Colab Notebook

12. If everything runs correctly you can skip to step 13, if not: Please see the error message provided by Google Colab and either follow the steps provided by Google Colab to resolve it.
If none are provided, google the error message and try to follow these steps.
One of the most common errors are caused by missing packages.
These errors can be resolved by running the '!pip install PACKAGE_NAME' command, before running the code, or '!pip install PACKAGE_NAME == VERSION_NUMBER' if a specific version of said package is required.
If this was indeed the case, restart the runtime after running this command, in order to ensure that Google Colab is aware of the newly installed package.

12. The resulting files will be saved as .wav files in the samples folder.
The first twenty files are the Harvard sentences, the other three are sentences we added to extend the testing range with some more natural sentences.
If you wish to create your own sentences, you can either add them to the document in similar fashion, or you can replace the current content of the file with your own sentences.
Note that, in case you do this, the first line of the file doesn't get read and every line should be preceded by a number followed by a dot.
Another option is to create a new text file in the repository and changing the test_data variable in the hyperparams.py file by the name of the new text file you created.
Here too holds that the first line won't get read, so beware of that!

*If you want to run the code again, make sure to restart the runtime, because Google Colab does not
remember which version of tensorflow it was running

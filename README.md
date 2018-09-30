# 10-fold artist-filtered cross-validation split for the Extended Ballroom Dataset

This repository contains a 10-fold cross-validation split of the Extented Ballroom Dataset. This split was created using a Python script and supplied metadata from the dataset [website](http://anasynth.ircam.fr/home/media/ExtendedBallroom). It complies to the following rules:

* Applies an artist filter: making sure that, for a given fold, no songs from the same artist are on the training and the test sets at the sime time.
* Applies a production filter, making sure that, for a given fold, no songs from the same disc are on the training and the test sets at the same time.

This is not a stratified split. The number of samples for some classes is simply too small, thus a stratified split would result in too few folds.  Plus, we wanted to play around with non-stratified datasets, thus the split.

## f*_train.txt files

These files contain the lists of the files that should be used to train the predictive models. The format is the following:

> song_file\\tgenre\\n

## f*_test.txt files

These files contain the lists of files that should be used to test the predictive models. The format is the following:

> song_file\\n

## f*_evaluate.txt files

These files contain the exact same list of files of the correspondent test file, except that they also contain the ground-truth:

> song_file\\tgenre\\n

If you use this split, please cite this page!

Cheers!

Juliano

Lecturer @ Universidade Tecnologica Federal do Parana (Campo Mourao, PR, Brazil) 

PhD Candidate @ UNICAMP (Campinas, SP, Brazil)

julianofoleiss *at* utfpr *dot* edu *dot* br



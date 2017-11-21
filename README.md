Chinese text classification algorithm based on cnn
Introduction

Reference to IMPLEMENTING A CNN FOR TEXT CLASSIFICATION IN TENSORFLOW to achieve a simple convolutional neural network for Chinese text classification tasks (this project uses the data set is the Chinese spam identification task data set).
the difference

The original blog cnn for English text classification, did not use word2vec to get the word vector expression, but added in the network embedding layer to get the vector.
This project is to use word2vec first to obtain the Chinese test data set of each word vector expression, and then enter the convolutional network for classification.

Method of operation

training

python train.py 

View summaries on tensorboard

run tensorboard --logdir / {PATH_TO_CODE} / runs / {TIME_DIR} / summaries / to view summaries in web view

Test, classification

run python eval.py --checkpoint_dir / {PATH_TO_CODE / runs / {TIME_DIR} / checkpoints}
If you need to categorize the files provided by yourself, change the relevant input parameters

If you need to test the accuracy, you need to specify the corresponding label file (input_label_file):
python eval.py --input_label_file / PATH_TO_INPUT_LABEL_FILE
Explanation: Each line in input_label_file is 0 or 1, corresponding to each line in input_text_file.
In eval.py, if there is this control tag file input_label_file, the prediction accuracy is output
Recommended operating environment

python 2.7.13 :: Anaconda 4.3.1 (64-bit)
tensorflow 1.0.0
gensim 1.0.1
Centos6 64bit

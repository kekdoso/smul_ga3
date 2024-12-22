# smul_ga3
Based on adanRiva's CNN-Audio-Classifier-with-Keras-Tensorflow repo (@ https://github.com/adanRivas/CNN-Audio-Classifier-with-Keras-Tensorflow/tree/master)

Execution steps:

1) Download the ESC-50 dataset and extract it to the workspace environment of the application (Ensure that "ESC-50-master" is the top path)
2) Run the save_melspectograms.ipynb file. This processes every sound into a mel-spectogram and performs test splitting of the dataset.
3) Run the TransferLearning_ESC50_Classifier.ipynb file. This is where the core model is.

Some notes for the execution of the model:
- A file with the weights of the trained model is available for faster execution.
- If a retraining of the model is desired, consider that a GTX 1060 6GB GPU was used in a WSL environment (~45 minutes). Training with the CPU is possible, but takes too long.

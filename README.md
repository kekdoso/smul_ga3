# smul_ga3 - Environmental Sound Classification
This project implements a CNN-based audio classifier for environmental sound classification using the ESC-50 dataset. It is inspired by and builds upon [adanRivas's CNN-Audio-Classifier-with-Keras-Tensorflow](https://github.com/adanRivas/CNN-Audio-Classifier-with-Keras-Tensorflow/tree/master).  

## Table of Contents  
- [Features](#features)
- [Execution Steps](#execution-steps)
- [Some notes for the execution of the model](#some-notes-for-the-execution-of-the-model)

## Features  
- **Mel-Spectrogram Preprocessing**: Converts audio signals into mel-spectrograms for CNN processing.  
- **Transfer Learning**: Leverages pre-trained models for efficient and accurate sound classification.  
- **Customizability**: Allows for model retraining or direct use of pre-trained weights.  

## Execution Steps:

- **Step 1**: Download the ESC-50 dataset and extract it to the workspace environment of the application (Ensure that "ESC-50-master" is the top path)
- **Step 2**: Run the save_melspectrograms.ipynb file. This processes every sound into a mel-spectrogram and performs test splitting of the dataset.
- **Step 3**: Run the TransferLearning_ESC50_Classifier.ipynb file. This is where the core model is.

The code in both files gives further instructions and insights into how the code should run to achieve our results. However, some of the files were too large to include in this repo and must be generated locally.

## Some notes for the execution of the model:
- Please be careful while using the model weights file on different test splits, as this might make accuracy and other metrics unrealible.
- If a retraining of the model is desired, consider that a GTX 1060 6GB GPU was used in a WSL environment (~45 minutes). Training with the CPU is possible, but takes too long.

## Library dependencies:
librosa==0.10.2.post1
matplotlib==3.10.0
numpy==2.2.1
pandas==2.2.3
pytest==8.3.4
seaborn==0.13.2
tqdm==4.67.1

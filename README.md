# smul_ga3 - Environmental Sound Classification
This project implements a CNN-based audio classifier for environmental sound classification using the ESC-50 dataset. It is inspired by and builds upon [adanRivas's CNN-Audio-Classifier-with-Keras-Tensorflow](https://github.com/adanRivas/CNN-Audio-Classifier-with-Keras-Tensorflow/tree/master).  

## Features  
- **Mel-Spectrogram Preprocessing**: Converts audio signals into mel-spectrograms for CNN processing.  
- **Transfer Learning**: Leverages pre-trained models for efficient and accurate sound classification.  
- **Customizability**: Allows for model retraining or direct use of pre-trained weights.  

---

## Execution steps:

### Step 1: Download the ESC-50 dataset and extract it to the workspace environment of the application (Ensure that "ESC-50-master" is the top path)
### Step 2: Run the save_melspectograms.ipynb file. This processes every sound into a mel-spectogram and performs test splitting of the dataset.
### Step 3: Run the TransferLearning_ESC50_Classifier.ipynb file. This is where the core model is.

## Some notes for the execution of the model:
- A file with the weights of the trained model is available for faster execution. However, this might make accuracy and other metrics unrealible, as the test splitting for the specific weights might be different and the model could be classifying sounds it was trained on.
- If a retraining of the model is desired, consider that a GTX 1060 6GB GPU was used in a WSL environment (~45 minutes). Training with the CPU is possible, but takes too long.

# RF-Fingerprint-CNN-Classifier

## Overview
This project focuses on constructing a classifier using Convolutional Neural Networks (CNN) to identify RF fingerprints. The process involves three main stages to create training and testing datasets.

## Stages

### Stage 1: Extracting Frames
- **File:** `Frame_Filter_A.ipynb`
- **Description:** Captures transmissions using software-defined radios (SDR). This stage removes unwanted noise periods (silence or irrelevant packets) and extracts the desired frames from specific devices.

### Stage 2: Filtering Corrupted Frames
- **File:** `Frame_Filter_B.ipynb`
- **Description:** Performs additional filtering on partially captured frames. It constructs a training set of 2000 samples and a testing set of 400 samples for each device, which are then concatenated.

### Stage 3: Preprocessing and Training
- **File:** `BLE_RF_CNN_Training.ipynb`
- **Description:** Implements preprocessing techniques as described in the associated paper and utilizes a proposed CNN classifier for training.

## Steps for Training

1. **Download the data** and navigate to the data directory (see Cell #2).
2. **Load the data** by running Cell #2.
3. To use the transient and preamble part, run Cell #3. To use the full-length raw IQ samples, skip Cell #3.
4. To apply any mentioned preprocessing techniques, uncomment the desired technique in Cell #4. To use raw IQ samples, skip Cell #4.
5. Adjust the CNN structure in the designated cell, modifying the model, hyperparameters, and/or optimizers as needed before starting the training.
6. Load your testing data. Ensure that the same preprocessing technique used for training is applied to the testing data for meaningful results.

## Author
Haytham Albousayri


## Contact
For questions or inquiries, please reach out to Haytham Albousayri at Albousah@oregonstate.edu.

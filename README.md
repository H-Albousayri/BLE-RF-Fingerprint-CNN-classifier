# RF-Fingerprint-CNN-Classifier

## Overview
This project focuses on constructing a classifier using Convolutional Neural Networks (CNN) to identify RF fingerprints to BLE Devices. The process involves three main stages to create training and testing datasets.

## Stages

### Stage 1: Extracting Frames
- **File:** `Frame_Filter_A.ipynb`
- **Description:** Captures transmissions using software-defined radios (SDR). This stage removes unwanted noise periods (silence or irrelevant packets) and extracts the desired frames from specific devices.

### Stage 2: Filtering Corrupted Frames
- **File:** `Frame_Filter_B.ipynb`
- **Description:** Performs additional filtering on partially captured frames. It constructs a training set of 2000 samples and a testing set of 400 samples for each device, which are then concatenated. This is how the each dataset looks like at the output of this stage:
<p align="center">
    <img src="https://github.com/user-attachments/assets/639411f7-f879-4d4a-9349-11655f53b3950" alt="Description" width="400" />
</p>



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

## References

Here are the citations you can use in your research:
```markdown
For a complete list of references, see [references.bib](path/to/references.bib).

# MRI Brain Tumor Classification using CNN
This project focuses on processing and analyzing MRI scans stored in the DICOM format to classify brain tumors using a Convolutional Neural Network (CNN). The dataset, sourced from the Cancer Imaging Archive, includes MRI scans from a single patient taken at two different time points, allowing for an examination of tumor progression following treatment.

# Dataset
[Cancer Imaging Archive: Brain Tumor Progression
](https://wiki.cancerimagingarchive.net/display/Public/Brain-Tumor-Progression)

# Project Goals
DICOM Image Processing: Load, visualize, and preprocess MRI images.

Metadata Extraction: Analyze metadata such as scan dates, modality, and imaging parameters.

CNN Implementation: Develop and train a deep learning model to classify MRI images based on tumor characteristics.

Tumor Progression Analysis: Compare images from two different time points to assess treatment effects.


# Methodology

### Data Preprocessing

Load and parse DICOM files using pydicom

Convert images to a standardized format for CNN training

Normalize pixel intensity values for improved model performance

### Exploratory Data Analysis

Visualize MRI scans to understand tumor progression

Extract and analyze metadata

### Model Development

Build a Convolutional Neural Network (CNN) using TensorFlow/Keras

Train the model on labeled MRI scans

Evaluate performance using accuracy, precision, recall, and F1-score

### Tumor Classification & Progression Detection

Classify tumors based on MRI images

Compare MRI scans before and after treatment to track progression


# Results & Insights
The CNN model classifies MRI images with high accuracy.

Tumor progression is assessed by comparing images before and after therapy.

The approach demonstrates the potential of deep learning in medical imaging.

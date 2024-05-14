# Neural Networks for Osteoarthritis Detection in Dogs

## Overview
This repository contains code and documentation for ECE 542 - Neural Networks and Deep Learning project conducted under the guidance of Dr. Edgar Lobaton, Dr. Masataka Enomoto, and Dr. Duncan Lascelles. The project aims to use neural networks to detect osteoarthritis (OA) in young dogs by analyzing their walking and trotting patterns to diagnose OA-related pain.

## Contents
- **Presentation Slides**: Contains the slides used for presenting the project, including background information on OA, dataset details, data selection process, model architectures (Random Forest, Convolutional Neural Network, Long Short-Term Memory), training configurations, and future directions.
  
- **Data Preprocessing Scripts**: Python scripts for preprocessing the provided dataset, including extracting features from `_M` and `_G` files, splitting the dataset into train-validation-test sets, and preparing the data for model training.

- **Model Implementation**: Jupyter notebooks and Python scripts for implementing and training the Random Forest, Convolutional Neural Network (CNN), and Long Short-Term Memory (LSTM) models. Includes code for data loading, model architecture definition, training, evaluation, and model visualization.

- **Results Analysis**: Code and notebooks for analyzing the results obtained from the trained models, including metrics calculation, performance comparison, and visualization of model predictions.

## Dataset
- **Source**: Provided by The NC State College of Veterinary Medicine.
- **Description**: Contains Center of Pressure (COP) data for approximately 120 dogs, spanning a range of ages and health statuses. Includes dogs with radiographic evidence of OA (rOA), dogs experiencing joint pain, and healthy dogs.
- **Format**: Dataset comprises both video recordings (AVI format) and Tekscan files (FSX format). The COP data is collected through walking and trotting trials using a pressure-sensitive walkway system (Tekscan).
- **Preprocessing**: Data preprocessing involves selecting dogs for analysis, splitting the dataset into train-validation-test sets, and extracting relevant features from the `_M` and `_G` files.

## Model Architectures
- **Random Forest**: A baseline model was built due to the absence of pre-existing baselines. Simple classifier results were studied.
- **Convolutional Neural Network (CNN)**: Utilized `_M` file data by combining all frames into a single frame and passing it as images to the CNN.
- **Long Short-Term Memory (LSTM)**: Chosen for its adeptness in capturing temporal dependencies in the dataset, which consists of temporal data due to multiple runs per dog.

## Training Configurations
- **Epochs**: 10
- **Batch Size**: 32
- **Window Size**: 120 (for LSTM)

## Future Directions
- Train CNN with more extracted data from `_M` files.
- Combine CNN and RNN architectures using a Multi-Layer Perceptron (MLP) to utilize features from both `_M` and `_G` files for improved results.

## Q&A
For any questions or inquiries, please reach out to the project contributors listed in the presentation slides.

## Explanation:
https://www.youtube.com/watch?v=LloZvyYQyU4&t=275s
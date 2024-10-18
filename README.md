# Discrete Key-Value Bottleneck

This is my attempt at recreating one of the models described in the paper titled "Discrete Key-Value Bottleneck" written by Frederik Träuble, Anirudh Goyal, Nasim Rahaman, Michael Mozer, Kenji Kawaguchi, Yoshua Bengio, and Bernhard Schölkopf.

## Repository Structure

Two files are present in this repository:
- **NUS_Final.ipynb**: This notebook implements a Key-Value Bottleneck model designed for classifying the MNIST dataset in a non-stationary learning environment. It compares the performance of the Key-Value Bottleneck model against a traditional Multi-Layer Perceptron (MLP) model. The non-stationary dataset is generated such that the model must adapt to pairs of classes sequentially, simulating a continual learning scenario.
- 

## Key Features

- **Key-Value Bottleneck Model**: Utilizes a discrete key-value mechanism to reduce the dimensionality of the input features while retaining critical information for classification.
  
- **MLP Baseline**: A simple multi-layer perceptron is used as a baseline for comparison.
  
- **Non-Stationary Dataset**: Organized to change the classes presented to the model over time, highlighting the ability of the Key-Value Bottleneck to mitigate catastrophic forgetting.
  
- **Performance Evaluation**: Includes functions to evaluate training and validation losses for both models, enabling direct performance comparison.

## Technical Specifications

- **Input Dimensions**: 784 (28x28 pixels)
  
- **Key-Value Bottleneck Configuration**:
  - Number of Keys: 2000
  - Key Dimension: 32
  - Value Dimension: 8
  
- **MLP Configuration**:
  - Hidden Layer Dimension: 32
  - Number of Classes: 8 (for digits 0-7)
  
- **Training Parameters**:
  - Batch Size: 32
  - Loss Function: Cross-Entropy Loss for classification
  - Optimizers:
    - Adam optimizer for MLP (learning rate: 0.001)
    - Adam optimizer for Key-Value Bottleneck model (learning rate: 0.0025)
  
- **Reproducibility**: A seed value is set (default is 42) to ensure consistent results across runs.


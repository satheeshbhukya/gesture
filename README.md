# Self-Supervised Learning for Gesture Classification using Contrastive Learning

This project implements self-supervised learning (SSL) using contrastive learning to classify gestures from sequential data (e.g., joint positions over time). The core of the model is a Long Short-Term Memory (LSTM) network that learns feature representations from gesture sequences without the need for labeled data. The learned representations are then used for downstream gesture classification tasks.

## Overview

The project demonstrates how contrastive learning can be used to train a model to recognize gestures by comparing pairs of similar (positive) and dissimilar (negative) gestures. The model learns to bring positive pairs closer together in the feature space and push negative pairs farther apart.

### Key Components:
- **Contrastive Encoder (LSTM-based)**: An LSTM model that encodes gesture sequences into feature vectors.
- **Contrastive Loss**: A loss function that drives the model to distinguish between similar and dissimilar pairs.
- **Pair Generation**: The data is transformed into pairs of similar (positive) and dissimilar (negative) gestures.
- **Gesture Classifier**: A classifier that uses the learned feature representations to predict the gesture class.

## Requirements

To run this project, you'll need the following Python packages:

- `torch` (PyTorch)
- `numpy`
- `matplotlib` (for visualizations)
- `scikit-learn` (optional, for evaluation)

You can install the required dependencies using:

```bash
pip install torch numpy matplotlib scikit-learn

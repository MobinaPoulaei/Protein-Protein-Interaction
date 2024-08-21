# Protein-Protein Interaction (PPI) Analysis using Graph Convolutional Networks (GCN)
This repository contains a Jupyter Notebook for analyzing Protein-Protein Interactions (PPI) using a Graph Convolutional Network (GCN). The notebook is designed to train a model on PPI data, validate its performance, and evaluate its effectiveness on a test dataset.

# Introduction
Protein-Protein Interactions (PPIs) are fundamental to most biological processes. Understanding these interactions can lead to insights into cellular functions, the mechanisms of diseases, and the development of new therapeutic strategies. This notebook aims to analyze PPIs by leveraging various computational tools and datasets.

#Notebook Overview
The notebook is structured as follows:

- **Data Preparation**: The notebook first loads and prepares the PPI dataset, splitting it into training, validation, and test sets.
- **Model Training**: The GCN model is trained using the training set, with the loss function and optimizer defined to handle class imbalance and improve model convergence.
- **Evaluation**: The model's performance is evaluated on the validation set during training, with the best model being saved for later testing.
- **Testing**: The final model is tested on a separate test dataset, and key metrics such as accuracy and F1 scores are computed.

# Model Architecture
The GCN model is designed as follows:

- **Two GCN Layers**: The model consists of two Graph Convolutional layers (GCNConv) to capture the graph structure and interactions between nodes (proteins).
- **Activation and Dropout**: ReLU activation functions and dropout layers are used to introduce non-linearity and prevent overfitting.
- **Output Layer**: A linear layer maps the learned representations to the output classes.

# Training Process
** Data Loading**: Training, validation, and test datasets are loaded and batched using PyTorch's DataLoader.
** Loss Function**: The BCEWithLogitsLoss is used, with class weights to address class imbalance.
** Optimizer**: The Adam optimizer is employed for model training.

# Results
- **Training and Validation Losses**: The training and validation losses are plotted to visualize the model's learning progress.
- **Test Accuracy and F1 Scores**: The final model achieves 91% accuracy and 84% F1 scores on the test set.

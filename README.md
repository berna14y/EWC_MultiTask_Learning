# EWC_MultiTask_Learning
Elastic Weight Consolidation for Multi Task Learning

The aim of the provided code is to implement the Elastic Weight Consolidation (EWC) algorithm for training a neural network on multiple tasks sequentially. The EWC algorithm is a method for enabling continual learning or lifelong learning, where a model learns multiple tasks over time without forgetting previously learned tasks.

In the context of this code, the aim is to train a neural network on the MNIST dataset for multiple tasks. Each task represents a different variation of the MNIST dataset. The tasks are defined by permuting the pixels of the images in different ways, creating variations of the original dataset.

The code performs the following steps:

1) Loads the MNIST dataset and creates variations of the dataset by permuting the pixels.
2) Defines a neural network model using convolutional and fully connected layers.
3) Implements the EWC algorithm for training the model on multiple tasks. The algorithm takes into account the Fisher information matrix, which measures the sensitivity of the model's parameters to changes in the loss function.
4) Trains the model on all tasks together, using the EWC algorithm to regularize the learning process and prevent catastrophic forgetting. The model is trained for multiple epochs on the concatenated training data from all tasks.
5) Tests the trained model on each task separately and calculates the accuracy.
6) Stores the average accuracy for each task in the offline_accs list.

   
By using the EWC algorithm, the aim is to train the model in a way that preserves the knowledge learned from previous tasks while adapting to new tasks. This enables the model to learn multiple tasks sequentially without significantly forgetting the previously learned tasks.

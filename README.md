# Transfer Learning with ResNet50 and Keras

This repository contains a Python script that demonstrates **transfer learning** using the powerful **ResNet50** convolutional neural network (CNN) architecture with the `tensorflow.keras` library. The script is designed for an image classification task with a new dataset.

---

## Core Concepts

### What is Transfer Learning?
Transfer learning is a machine learning technique where a model trained on a large dataset for one task is reused as a starting point for a model on a different, but related, task. The idea is to leverage the features the model has already learned, saving significant time and computational resources.

### ResNet50
ResNet50 is a widely used CNN architecture that was pre-trained on the **ImageNet** dataset, a massive collection of over 14 million images categorized into 1000 classes. The model has learned a rich hierarchy of features, from basic edges and textures in its initial layers to complex object parts in its deeper layers.

### Feature Extraction vs. Fine-Tuning
The script uses a two-phase training strategy, combining two common transfer learning methods:

- **Feature Extraction:** The pre-trained layers of ResNet50 are frozen (their weights are not updated). Only a newly added, custom classification head is trained. This is efficient as the model's core feature-learning capabilities are already strong.  

- **Fine-Tuning:** After the initial training, the script unfreezes a few of the top layers of the pre-trained model and trains the entire model again with a very low learning rate. This allows the model to make small, precise adjustments to the pre-trained weights, adapting them specifically to the new dataset.

---


# Implementing a CNN for CIFAR-10

## ** Dataset Preparation**
- CIFAR-10 was loaded (from Hugging Face or built-in datasets).
- Images were **normalized** to the `[0,1]` range and labels **one-hot encoded**.
- The dataset was split into **training (80%)** and **testing (20%)** subsets.

## ** CNN Model Architecture**
A CNN was built using TensorFlow/Keras with the following layers:
- **Convolutional Layers** with ReLU activation for feature extraction.
- **MaxPooling Layers** for spatial dimensionality reduction.
- **Fully Connected Layers** culminating in a softmax output for classification.

## ** Training and Evaluation**
Two models were trained:
1. **Without Data Augmentation**: Trained on raw CIFAR-10 images.
2. **With Data Augmentation**: Used random rotations, flips, and shifts.

- **Loss vs Accuracy Curves:** Plotted to visualize model performance.
- **Confusion Matrices:** Generated to analyze misclassification patterns.

## ** Ablation Study on Hyperparameters**
Experiments were conducted by varying:
- **Learning Rate**: (e.g., 0.001, 0.01, 0.1)
- **Batch Size**: (e.g., 16, 32, 64)
- **Number of Convolutional Filters**: (e.g., 16, 32, 64)
- **Number of Convolutional Layers**

Comparative analysis of performance and convergence trends was performed.

## ** Error Analysis**
- Confusion matrices for both models were examined.
- Some categories were more frequently misclassified, suggesting potential improvements through:
  - Additional **regularization**
  - **Fine-tuning** the network
  - **Using a deeper architecture**

# Linear_Classification

This model is a binary classification neural network built using PyTorch to predict whether a breast cancer tumor is malignant or benign based on input features from the breast cancer dataset. Here is a summary of the steps and components involved:

1. **Data Loading and Preparation**:
   - The breast cancer dataset from `sklearn.datasets` is loaded. This dataset contains 569 samples with 30 features each, and the target labels are binary (0 for benign, 1 for malignant).
   - The data is split into training and testing sets using `train_test_split`.

2. **Data Scaling**:
   - The features are scaled using `StandardScaler` to ensure they have zero mean and unit variance, which is crucial for training neural networks efficiently.

3. **Model Definition**:
   - A simple feedforward neural network is defined using `nn.Sequential`. The model consists of a single linear layer followed by a sigmoid activation function. This structure maps the 30 input features to a single output value between 0 and 1, representing the probability of the tumor being malignant.

4. **Loss Function and Optimizer**:
   - The Binary Cross-Entropy Loss (`nn.BCELoss`) is used as the loss function since this is a binary classification problem.
   - The Adam optimizer is used to update the model parameters during training.

5. **Data Conversion**:
   - The training and testing data are converted to PyTorch tensors to be used in the model training process.

6. **Training Process**:
   - The model is trained for 1000 epochs. In each epoch:
     - The gradients are zeroed.
     - A forward pass is performed to compute the outputs and the loss.
     - A backward pass is performed to compute the gradients.
     - The optimizer updates the model parameters.
   - Both training and testing losses are computed and stored for each epoch.
   - Training and testing accuracies are also computed and stored for each epoch.

7. **Performance Evaluation**:
   - After training, the model's performance is evaluated in terms of accuracy on both the training and testing sets.
   - Loss and accuracy per iteration are plotted to visualize the training process.

8. **Results**:
   - The final training and testing accuracies are printed, providing a measure of how well the model performs on unseen data.

The goal of this model is to classify whether a given breast cancer tumor is malignant or benign based on its features, providing a useful tool for medical diagnosis. The training process helps the model learn from the data, and the evaluation ensures that the model performs well on new, unseen data.

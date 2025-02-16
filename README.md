# Constructing Convolutional Neural Networks on EMNIST

* <h4><b> Overview </b></h4> 

  In this project, the focus is on constructing Convolutional Neural Networks (CNNs) for handwritten letter classification using the Extended MNIST (EMNIST) dataset, which includes both digits and uppercase letters. The project involves preprocessing the EMNIST dataset, building and training custom CNN architectures, and evaluating the models' performance on the test set. The models are compared based on accuracy and loss metrics, and techniques such as data augmentation and dropout are explored to improve model robustness. The project highlights the challenges of classifying handwritten letters and digits and provides insights into optimizing CNN architectures for such tasks.

* <h4><b> Key Findings </b></h4> 

  - <b> Data Augmentation Improves Model Performance: </b> By applying data augmentation techniques such as rotation and flipping to the EMNIST dataset, the CNNs showed improved generalization and higher accuracy on the validation and test sets, reducing overfitting.
  - <b> Model Complexity Impacts Performance: </b> Increasing the depth of the CNN with more convolutional layers and filters led to better feature extraction, resulting in higher accuracy. However, adding too many layers also increased the model’s training time and complexity.
  - <b> Dropout Regularization Reduces Overfitting: </b> The implementation of dropout layers effectively reduced overfitting by randomly setting a fraction of input units to zero during training, improving model performance on unseen data.
  - <b> Learning Rate Plays a Critical Role: </b> The choice of learning rate significantly impacted the training process. A learning rate that was too high led to unstable training, while a lower learning rate improved convergence but required more epochs to reach optimal performance.
  - <b> Model Evaluation Highlights the Difficulty of Handwritten Letter Recognition: </b> The CNN model achieved higher accuracy on digit classification but struggled with letter recognition, pointing out the inherent complexity in distinguishing similar-looking handwritten uppercase letters.

* <h4><b> Insightful Details </b></h4> 

  - <b> Custom CNN Architecture – </b> The model uses multiple convolutional layers with increasing filter sizes, followed by max-pooling layers, and dense layers for classification. This architecture allows the model to efficiently learn hierarchical features from raw pixel data in the EMNIST dataset.
  - <b> Batch Normalization for Stability – </b> Batch normalization is applied after each convolutional layer, improving the model’s training stability and accelerating convergence by normalizing activations. This helps avoid internal covariate shift during training.
  - <b> Activation Function Choice – </b> The ReLU (Rectified Linear Unit) activation function is used in the convolutional layers, providing non-linearity to the network and allowing it to learn complex patterns in the handwritten letters. The softmax activation is used in the output layer for multi-class classification.
  - <b> Training with Cross-Entropy Loss – </b> The categorical cross-entropy loss function is used for training the model, which is appropriate for multi-class classification tasks, ensuring the model minimizes the difference between predicted and actual class distributions during optimization.
  - <b> Performance Evaluation with Accuracy Metrics – </b> The model’s performance is tracked through accuracy on both the training and validation datasets. Additionally, visualizations of the loss and accuracy curves provide a clear view of model convergence, helping identify when the model begins to overfit or converge prematurely.
 
* <h4><b> Challenges </b></h4> 

   - <b> Overfitting on Small Datasets – </b> With limited data, the model might overfit during training, especially if there isn’t enough regularization or if the network is too complex. This results in high accuracy on training data but poor generalization to validation data.
   - <b> Data Imbalance in EMNIST – </b> The EMNIST dataset might have imbalanced classes, where some letters are underrepresented. This could lead to a bias in the model’s predictions, with the network favoring more frequent classes.
   - <b> Choosing Hyperparameters – </b> Tuning hyperparameters like the number of filters, kernel sizes, and learning rate is a challenge. Inadequate choices can lead to poor convergence or failure to train effectively, requiring extensive experimentation.
   - <b> Convergence Issues with Deep Networks – </b> As the CNN architecture becomes deeper, it can be challenging to achieve stable convergence. Layers can start to saturate or lead to vanishing/exploding gradients, especially without techniques like proper initialization or using Batch Normalization.
   - <b> Computational Resources – </b> Training a deep neural network on a large dataset like EMNIST requires significant computational power, especially when using multiple convolutional layers. Training can be slow on machines with limited GPU or CPU power, making it time-consuming to experiment with different architectures.

* <h4><b> Data Files </b></h4> 

  - <b> Dataset for the project – </b> [Download Dataset]()
  - <b> Code for the project – </b> [View Code](https://github.com/Hamza-Siam/Hamza-Siam/blob/main/Constructing%20Convolutional%20Neural%20Networks%20on%20EMNIST.pdf)

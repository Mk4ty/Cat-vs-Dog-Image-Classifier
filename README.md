# Cat-vs-Dog-Image-Classifier
Objective:
To build a binary image classification model using a Convolutional Neural Network (CNN) that can accurately distinguish between images of cats and dogs.

Project Description:
1. Dataset Handling:

Content: Contains labeled images of cats and dogs divided into training and test directories.

2. Data Preparation:

 TensorFlow Image Generators:
 image_dataset_from_directory() was used to automatically load, label, and batch images.
 Both training and validation datasets were resized to (256x256) pixels and batched with size 32.
 Normalization: Pixel values were scaled to the range [0, 1] using a custom preprocessing function to improve model performance and convergence.

3. Model Architecture:

 A deep CNN model was built using Keras’ Sequential API. The architecture includes:

Convolutional Layers: Three convolutional layers with increasing filters (32, 64, 128) followed by Batch Normalization and MaxPooling to capture spatial hierarchies and reduce   overfitting.

Flattening Layer: Transforms the 3D feature maps into 1D feature vectors.

Dense Layers: Fully connected layers with 128 and 64 neurons, followed by dropout (10%) for regularization.

Output Layer: A single neuron with sigmoid activation for binary classification (Cat or Dog).

4. Model Compilation and Training:

 Loss Function: binary_crossentropy suited for two-class problems.
 Optimizer: Adam for efficient gradient descent.
 Metrics: Accuracy was used to monitor training.
 Epochs: Model trained for 10 epochs with validation on the test set.

5. Evaluation and Visualization:

 Training and validation accuracy were plotted using matplotlib to analyze model learning trends and potential overfitting.

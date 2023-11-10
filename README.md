# Vgg_On_Oct_Classification
This is a simple implementation of Vgg for oct image classification

## Introduction
This project aims to classify Optical Coherence Tomography (OCT) images of the eye into one of four classes: `Normal`, `Diabetic Retinopathy (DR)`, `Glaucoma`, or `Age-related Macular Degeneration (AMD)`. It utilizes the VGG architecture to achieve accurate classification.

## Technologies Used
- Python
- TensorFlow
- Keras
- numpy
- pandas
- PIL
- matplotlib

## Dataset
The dataset used for this project is the OCT2017 dataset, which consists of images of the retina from patients with various eye conditions. The dataset can be downloaded from this [link](https://data.mendeley.com/datasets/rscbjbr9sj/3). The images are divided into train and test sets, with each set containing subdirectories for each class of eye condition.

## Preprocessing
- The provided images are resized to (256, 256) and normalized to values between 0 and 1.
- Data augmentation techniques such as random rotations, zooms, and flips are applied to the training set to increase the diversity of the data and improve the model's ability to generalize.

## Model Architecture
- The VGG architecture is utilized for this project, with slight modifications to match the input size of the OCT images.
- The model consists of convolutional layers followed by max pooling and fully connected layers.
- The output layer consists of 4 nodes, each representing one of the eye conditions.

## Model Training
- The model is trained for 50 epochs using a batch size of 32 on the augmented training data.
- Early stopping is utilized to stop training if the validation loss does not improve for 3 epochs.
- Model checkpoints are saved to keep track of the best model based on validation loss.
- Learning rate reduction is implemented to reduce the learning rate if the validation loss plateaus.

## Model Evaluation
- The trained model is evaluated using the test set.
- The accuracy and loss of the model on the test set are calculated.
- The loss and accuracy curves are plotted for both the training and validation sets.

## Conclusion
- The VGG model proved to be effective in classifying OCT images into different eye conditions.
- The model achieved high accuracy on the test set, demonstrating its ability to generalize well.
- The loss and accuracy curves show that the model is learning effectively and not overfitting.
- Further improvements can be made by fine-tuning the model, experimenting with different architectures, or using other pre-trained models such as ResNet or Inception.

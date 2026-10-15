# Practical 3: Autoencoder and Variational Autoencoder (VAE)

## About the Practical

In this practical, I explored how Autoencoders and Variational Autoencoders work using deep learning. The main aim was to understand how a neural network can learn important features from images and reconstruct them with as much accuracy as possible.

I used the MNIST dataset, which contains handwritten digits from 0 to 9. By training these models, I learned how images can be compressed into a smaller representation and then reconstructed from that representation.

## Objectives

- Understand the basic working of an Autoencoder.
- Learn how an encoder compresses an image into a smaller representation.
- Understand how a decoder reconstructs the original image.
- Explore the working of a Variational Autoencoder (VAE).
- Compare the reconstruction results of Autoencoder and VAE models.
- Evaluate the models using loss and reconstruction error.

## Dataset

For this practical, I used the **MNIST handwritten digit dataset**. Each image is a grayscale image of size 28 × 28 pixels.

Before training, I converted the images into floating-point values, normalized the pixel values between 0 and 1, and added a channel dimension. I also divided the data into training, validation, and testing sets.

## Technologies Used

- Python
- TensorFlow and Keras
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- Scikit-image

## Implementation

### 1. Autoencoder

An Autoencoder consists of two main parts:

- **Encoder:** Compresses the input image into a smaller latent representation.
- **Decoder:** Uses the compressed representation to reconstruct the image.

In this practical, I built a convolutional Autoencoder using CNN layers. I trained it to reproduce the input images and used reconstruction loss to measure how closely the output matched the original image.

### 2. Variational Autoencoder (VAE)

A Variational Autoencoder is similar to an Autoencoder, but it learns a probability distribution in the latent space instead of producing only a fixed compressed representation.

The VAE uses the learned mean and variance to sample latent vectors. This helps it learn a more structured latent space and makes it useful for generating new data.

I implemented the VAE using TensorFlow and Keras, with reconstruction loss and a KL-divergence term to guide the training process.

## Model Training and Evaluation

Both models were trained using the MNIST images. I used the Adam optimizer and included callbacks such as Early Stopping and ReduceLROnPlateau to help manage training.

I evaluated the Autoencoder using test loss, Mean Squared Error (MSE), and Mean Absolute Error (MAE). I also plotted the training and validation losses and compared original images with their reconstructed versions.

For the VAE, I monitored the total loss and its components to understand how well the model learned to reconstruct the input data.

## What I Learned

Through this practical, I understood how deep learning models can learn useful representations of images without needing to predict their class labels.

I also learned the difference between a traditional Autoencoder and a Variational Autoencoder. The Autoencoder focuses on compressing and reconstructing inputs, while the VAE learns a probabilistic latent space that can also support data generation.

Working with reconstruction images and loss curves helped me understand how model performance can be evaluated in practice.

## Conclusion

This practical gave me hands-on experience with building and training Autoencoder and Variational Autoencoder models. Using the MNIST dataset helped me observe how both approaches learn image representations and reconstruct handwritten digits.

Overall, I gained a better understanding of latent representations, reconstruction loss, and the role of VAEs in generative deep learning.

## Student Information

- **Name:** Soham Sabane
- **PRN:** 202401110070
- **Batch:** A3
- **Class:** T.Y. B.Tech
- **Department:** CSE AIML
- **Institute:** MIT Academy of Engineering (MIT AOE)
- **Course:** Generative AI Lab
- **Practical:** 3 — Autoencoder and Variational Autoencoder

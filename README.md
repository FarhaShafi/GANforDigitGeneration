# GANforDigitGeneration

## Objective
To implement and train a simple Generative Adversarial Network (GAN) using TensorFlow (Keras API) to generate handwritten digit images that resemble the MNIST dataset. This mini-assignment aims to strengthen your understanding of adversarial learning and generative modeling.

## Dataset
MNIST dataset available in TensorFlow

## Steps Involved
1. Build and train a GAN model using TensorFlow 2.x (Keras API) consisting of:
    - Generator Network: Takes a random noise vector (e.g., 100-dimensional) and outputs a 28×28 grayscale image.
    - Discriminator Network: Classifies input images (real or generated) as true (1) or fake (0).

2. Normalize the data to the range [-1, 1] and reshape to (28, 28, 1).
3. Model Design
    - Generator:
        Layers: Dense → BatchNormalization → LeakyReLU → Conv2DTranspose → Output (Tanh)
    - Discriminator:
        Layers: Conv2D → LeakyReLU → Dropout → Flatten → Dense (Sigmoid)
    - Loss Function: Binary Cross-Entropy (BCE)
    - Optimizer: Adam (learning rate = 0.0002, β1 = 0.5)
    - Train for at least 20 epochs and visualize the progress.
4. Output
    - Display a grid of generated digit images every few epochs.
    - Plot loss curves for generator and discriminator.
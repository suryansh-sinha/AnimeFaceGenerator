# AnimeFaceGenerator

PyTorch implementation of the DCGAN introduced in the paper ["Unsupervised Representation Learning with Deep Convolutional Generative Adversarial Networks"](https://arxiv.org/abs/1511.06434) by Radford et al. on the Anime Faces Dataset by McKinsey666.

# DCGAN

DCGAN, introduced by Radford et al. in 2015, is a seminal work in the field of generative models. Its key contributions are as follows:

1. Architecture Guidelines:
- DCGAN replaces fully connected layers with convolutional layers in both the generator and discriminator. 
- It employs batch normalization to stabilize training.
- Pooling layers are removed, and strided convolutions are used for downsampling.
- ReLU activation functions are used in the generator (except for the output layer, which uses tanh).
- LeakyReLU activation functions are employed in the discriminator.
2. Stable Training:
- DCGAN demonstrates that following the architectural guidelines leads to more stable training of GANs.
- It mitigates issues like mode collapse and vanishing gradients.
3. Image Synthesis:
- DCGAN achieves impressive results in generating high-quality images.
- It can synthesize realistic images from random noise vectors.
4. Latent Space:
- The generator learns a meaningful latent space where different directions correspond to distinct features.
- By interpolating between points in this space, smooth transitions between generated images can be created.

The generator architecture as shown in the paper -
![architecture.png](https://raw.github.com/suryansh-sinha/AnimeFaceGenerator/main/architecture.png)

# Anime Faces Dataset
The Anime Face Dataset was created by Mckinsey666. This dataset has 63,632 "high-quality" anime faces.

The data has been preprocessed using `torchvision.transforms` by resizing, cropping and normalizing the images.

# Training
I have trained the model using the hyperparameters used in the original paper. Feel free to play with the parameters in the colab notebook. I am planning to convert this notebook into individual scripts in the future!

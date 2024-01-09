# Deep Learning Image Colorization (2023)

This project transforms gray-scale images into color images using a Generative Adversarial Network (GAN) deep learning architecture.

## Technologies
Python, PyTorch

## Dataset

The dataset chosen for this project was the Flickr8K dataset
which is a collection of 8,000 images that have been posted
on the image and video hosting service, Flickr. The more
popular dataset, Flicker30K, is also a collection of images
posted on the media platform.

While this dataset was selected for this project, any dataset
consisting of color images can be used. Some other examples
include, but are not limited to, the following:

- ImageNet ctest10k: Consists of a subset of approx-
imately 10,000 images from the ImageNet dataset
(14,000,000 images) that have been converted to gray-
scale to create color and gray-scale image pairings for
colorization tasks.

- Flickr-Faces-HQ (FFHQ): Consists of approximately
52,000 images of human faces with different genders,
ages, ethnicities, accessories, and image backgrounds.

- CIFAR-100: Consists of approximately 60,000 images
with 100 different image classes.

### RGB VS Lab Color Channels

This image colorization model uses gray-scale images specifically
formatted using a Lab color space instead of the more popular color
space, RGB. LAB images are composed of three channels, Lightness (L),
Green-Red (A), and Yellow-Blue (B). The L channel encodes how light
each image is, the A channel encodes how green or red each pixel is,
and the B channel encodes how yellow or blue each pixel is. LAB format
is commonly used in image colorization tasks because, using the L channel
as input, the model can predict the other A and B channels. This reduces
the number of parameters necessary in a model that uses RGB format. If
RGB format were used, all three channels would need to be predicted instead,
R, G, and B.

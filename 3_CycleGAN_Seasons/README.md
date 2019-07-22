# CycleGAN Seasons

<p align="center">
  <image src="output/4000.png" height="75%" width="75%">
</p>

This project is my implementation of [CycleGAN](https://github.com/junyanz/CycleGAN). The **two generator and two discriminator architecture** was implemented for the GAN to convert images of size (128, 128, 3) from one domain to another or vice versa. The most impressive thing about CycleGAN is that it uses dual generators and **Cyclic-Consistency Loss** (difference between domain X and X->Y->X) to achieve gorgeous results without needing a single pair data (**semi-supervised learning**). 

The pictures above were results of this architecture trained on summer and winter images of the Yosemite National Park. Therefore, the generators are able to convert an unseen summer image to a winter image and the other way around. Despite having two generator and two discriminator networks, the logic behind CycleGAN is relatively easy to understand, which can be found [here](https://medium.com/coding-blocks/introduction-to-cyclegans-1dbdb8fbe781). 

While the discriminator is a simple convolutional classifier, the generator has a more interesting architecture. It consists of an encoder with 3 down-sizing layers, 6 residual block for deeper learning, and a decoder for 3 up-sizing layers. I think of it as compressing an image in domain one while learning about its spatial information, ensure more information learned by the residual nets, and use the information to expand the image again into domain two. 

# Folders

`output` contains the results that the generator made at different epochs.\
`samples_cyclegan` contains all of the results from every epoch.\
`checkpoints_cyclegan` contains both discriminator and both generator models.

# Papers

[Unpaired Image-to-Image Translation using Cycle-Consistent Adversarial Networks](https://arxiv.org/pdf/1703.10593.pdf)\
[Unsupervised Representation Learning with Deep Convolutional Generative Adversarial Networks](https://arxiv.org/pdf/1511.06434.pdf)\
[Least Square Generative Advarsarial Networks](https://arxiv.org/pdf/1511.06434.pdf)\
[Deep Residual Learning for Image Recognition](https://arxiv.org/pdf/1512.03385.pdf)

# Celebrity Face Generator

<p align="center">
  <image src="output/result2.png" width="75%" height="75%">
    <image src="output/result.png" width="75%" height="75%">
<p>

Human faces have very complex featrues that are very difficult to extract. In this project, I used a [Celebrity Face Recognition Dataset](https://github.com/prateekmehta59/Celebrity-Face-Recognition-Dataset) as my input data. In my model, I used 4 convolutional and 4 transpose convolutional layers for the discriminator and generator architectures respectively. After training for 30 epochs batch size 128, the generator is able to make human faces with well defined features of dimension (32, 32, 3). Despite the pixelation due to my lack of time to train more longer periods, the hyperparameters and neural network model are shown to be effective as most generated faces are hard to distinguish from real.

# Papers

[Generative Adversarial Networks](https://arxiv.org/abs/1406.2661)

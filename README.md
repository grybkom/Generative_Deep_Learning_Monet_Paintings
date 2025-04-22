# GAN for Image Style Transfer of Paintings by Claude Monet
This project builds and trains a generative adversarial network (GAN) to transform real-world photos into images that resemble the painting style of Claude Monet.

---
**Background**
Generative Adversarial Networks (GANs) consist of two neural networks:  
- **Generator** – learns to produce realistic images in Monet's style.  
- **Discriminator** – learns to distinguish between real Monet paintings and generated images.

They are trained in a zero-sum game: the generator tries to fool the discriminator, while the discriminator gets better at identifying fakes.

The goal is to generate 7,000–10,000 images that closely mimic Monet’s artistic style.

---

**Architecture:**
- **Generator:**
  - Encoder → Bottleneck → Decoder architecture
  - Downsampling with convolutional layers
  - Upsampling with transposed convolutions
- **Discriminator:**
  - Spectral Normalization to improve training stability
- **Loss Functions:**
  - Adversarial Loss (standard GAN loss)
  - Perceptual Loss calculated using a pre-trained VGG network

**Data & Methodology:**

- The data used for this work is available at Kaggle as part of the competition, I’m Something of a Painter Myself.
  - 300 Monet paintings sized 256x256 in JPEG format
  - 7028 photos sized 256x256 in JPEG format
  - Amy Jang, Ana Sofia Uzsoy, Phil Culliton. (2020). I’m Something of a Painter Myself. Kaggle. https://kaggle.com/competitions/gan-getting-started

- **Languge:** Python
  - [PyTorch](https://pytorch.org/)
  - [Torchvision](https://pytorch.org/vision/stable/index.html)

**Examples of Generated Images**

![monet_3315](https://github.com/user-attachments/assets/a74db28d-ac0a-4e0d-ba02-329d9a7a525b)
![monet_5341](https://github.com/user-attachments/assets/a2eccaa7-2125-428d-aeeb-4f3f8497c87d)
![monet_0775](https://github.com/user-attachments/assets/d83c936b-9d8e-450b-8e97-0f7b680e5f1a)
![monet_6690](https://github.com/user-attachments/assets/a82d482b-8458-40a5-8cfc-e241da803ba3)
![monet_4622](https://github.com/user-attachments/assets/a01c1f0e-47ff-4ed0-8241-62ce35e0c26b)
![monet_4322](https://github.com/user-attachments/assets/55dd79d3-bb1c-48b8-991b-0a806d9bce16)




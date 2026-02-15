# Task 05: Neural Style Transfer (NST)

This project implements the algorithm described in *"A Neural Algorithm of Artistic Style"* by Leon A. Gatys. It uses the VGG-19 deep convolutional network to perform style transfer between two images.

## 🎨 How it Works
The model doesn't "train" in the traditional sense. Instead, it starts with the content image and performs **Gradient Descent** on the pixel values themselves to minimize a multi-part loss function:

* **Content Loss:** Calculated using the feature maps from `conv4_2`.
* **Style Loss:** Calculated using the [Gram Matrix](https://en.wikipedia.org/wiki/Gramian_matrix) of multiple layers to capture multi-scale textures.

## 🚀 Usage
1. **Requirements:** `torch`, `torchvision`, `Pillow`.
2. **Command:**
   ```bash
   python style_transfer.py --content content.jpg --style style.jpg

# 📊 Parameters
- content_weight: (Default 1) Importance of maintaining the original image structure.

- style_weight: (Default 1e6) Importance of applying the artistic style.
---
# Author
- Name: Pruonh Kimliya
- Email: kimliyapruonh@gmail.com

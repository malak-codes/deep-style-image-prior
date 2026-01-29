# Deep Style Image Prior: GAN Inversion & Image Restoration

This repository contains an implementation of **GAN Inversion** and **Image Restoration** techniques using the **StyleGAN2-ADA** architecture. The project explores how to map existing images back into the latent space of a pre-trained GAN and use that "prior" knowledge to restore degraded images.

## Project Overview

The core objective of this project is to leverage the powerful generative capabilities of StyleGAN2 as an "image prior." By optimizing a latent vector to match a target image, we can perform various image processing tasks, including denoising, super-resolution, and inpainting.

### Key Features

- **GAN Inversion**: Optimizing the latent vector $w$ to reconstruct a given target image using a pre-trained StyleGAN2-ADA model.
- **Image Restoration**: Restoring images from various degradations (e.g., noise, blur, downsampling) by performing inversion through the degradation process.
- **Perceptual Loss**: Utilizing a VGG16-based perceptual loss (LPIPS) to ensure high-quality, visually realistic reconstructions.
- **Latent Space Regularization**: Implementing regularization techniques to keep the optimized latent vectors within the distribution of the pre-trained model.

## Repository Structure

| File | Description |
| :--- | :--- |
| `deep_style_image_prior.ipynb` | The main Jupyter notebook containing the implementation of GAN inversion and restoration experiments. |
| `README.md` | Documentation providing an overview of the project and its components. |
| `LICENSE` | MIT License for the project. |

## Requirements

The project is designed to run in a GPU-accelerated environment (e.g., Google Colab) and requires:
- `torch` (PyTorch)
- `numpy`
- `matplotlib`
- `PIL` (Pillow)
- `StyleGAN2-ADA PyTorch` (automatically downloaded in the notebook)

## Usage

The implementation is provided as a Jupyter notebook. To run the experiments:
1. Open `deep_style_image_prior.ipynb` in Google Colab or a local Jupyter environment with a GPU.
2. Follow the cells to download the pre-trained checkpoints and run the latent optimization.
3. Experiment with different degradation modes to see how the GAN prior handles image restoration.

## License

This project is licensed under the **MIT License**. See the `LICENSE` file for details.

## Authors
- Malak

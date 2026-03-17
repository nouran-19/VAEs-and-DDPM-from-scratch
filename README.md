# VAEs-and-DDPM-from-scratch
Implementing VAEs (Variational Auto Encoders) and DDPM (Denoising Diffusion Probabilistic Model) from-scratch, rained on a targeted 3-class subset of the CIFAR-10 dataset (for low specs devices) and comparison through computationally aligned comparison

Here is a completely structured skeleton for your README.md based on your project files. It includes the environment requirements, a step-by-step replication guide, and the academic resources discussed earlier. 

## 🛠️ Requirements & Setup

To replicate this environment, you will need Python 3.8+ and the following libraries. 

Install the required packages using pip:
```bash
pip install torch torchvision torchmetrics matplotlib tqdm numpy
```

##  Replication Guide
Running the notebooks in the following order:

### 1. Train the VAE
Open and run VAE_Basic.ipynb.
* This notebook constructs a Convolutional VAE.
* It trains the model for 100 epochs.
* Generates latent space samples and saves the final model weights to vae.

### 2. Train the DDPM
Open and run Diffusion_Basic.ipynb.
* Constructs the Forward Noise Schedule and the Reverse U-Net with Sinusoidal Time Embeddings.
* Trains the model to predict added noise step-by-step.
* Generates samples via the reverse Markov chain and saves weights to ddpm.

### 3. Compare the Models
Open and run Models_Comparison.ipynb.
* Loads the saved model states for both VAE and DDPM.
* Generates side-by-side visual comparisons.
* Computes mathematical quality metrics using (KID and FID) to quantitatively evaluate which model produces higher fidelity images.

# BVAE-tf
Disentangled Variational Auto-Encoder in TensorFlow (Beta-VAE)
## Example Reconstructed Image
![alt text](https://github.com/shadySource/BVAE-tf/raw/master/images/reconstructed.png)

## What has beed done
* darknet 19 (fully convolutional & fast) encoder and decoder
* Custom keras sampling layer for sampling the distribution of variational autoencoders
* Custom loss in sampling layer for latent space regularization
    * Options are no reg, vae reg (kl divergence), or bvae reg (beta*kl-divergence)
    * You can also set a target capacity for dimension usage of the latent space
* Simple interface for setting up your own VAE or B-VAE
    * See [the test function in ae.py](https://github.com/shadySource/BVAE-tf/blob/0374800376cf74f9ad2eb2f7d8cfeedfe71a4a17/bvae/ae.py#L22) for usage information

## Enviroment Setup
I am using conda to ensure the enviroment is easy to install

0. Install [Anaconda](https://www.anaconda.com/download/) or
[Miniconda](https://conda.io/miniconda.html) (the python 3 version) for your platform
1. Recreate the conda environment from the yml:
``` conda env create -f environment.yml ```
2. Active the enviroment
    1. Windows: ```activate bvae-tf```
    2. Linux: ```source activate bvae-tf```

If you do not want to / cannot use conda, I am using tensorflow 1.4.0; see the environment.yml for more package info.

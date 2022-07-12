# Generating synthetic chest X-ray images using WGAN-GP
Generating synthetic chest X-ray images using [WGAN-GP](https://arxiv.org/abs/1704.00028)

In this repository, you can find three notebooks you can use to generate fake x-rays. 
You need the [NIH Chest X-rays dataset](https://www.kaggle.com/datasets/nih-chest-xrays/data).

`preprocess-nih-chest-full-64.ipynb` takes care of the preprocessing. In this case, we resize the images to a spatial resolution of 64x64. We also extract the labels.
In `train-gan-chest-xrays-64.ipynb`, you can train the GAN. Using a GPU for this is highly recomended.
We inspect the trained model in `evaluate-gan-chest-xrays-64.ipynb`. The notebook includes a interactive section where you can control how the fake image is generated. This is also shown in `controllable-generation.mp4`.

I used [Kaggle](https://www.kaggle.com/) to run the code.  
Python 3.7.12 | TensorFlow 2.6.4  
For training: Tesla P100-PCIE-16GB | CUDA 11.4 


You can use `evaluate-gan-chest-xrays-64.ipynb` directly by downloading the notebook to your working directory along with `generator.h5` and `discriminator.h5`.
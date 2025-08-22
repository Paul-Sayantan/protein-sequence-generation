### Protein Sequence Generation with Generative AI
This project explores generative deep learning models for synthetic protein sequence generation. Using the UniProt database, we trained and evaluated several architectures—including dense and convolutional autoencoders, plus their variational forms.
Our best-performing model, a convolutional variational autoencoder, achieved the lowest reconstruction error. We found that latent space size (condensation level) strongly affects sequence identity and diversity. At 80% condensation, the model generates diverse yet biologically meaningful protein variants.

This repository includes:<br>
Model training and generation notebooks<br>
Preprocessing scripts<br>
Example datasets<br>
Instructions for reproducing results and generating new sequences<br>

Generative AI holds strong promise for advancing protein engineering—and this repo is your starting point.<br>

### Paper
For an in-depth overview of our methodology and results, refer to the full paper accepted for publication in IEEE Conference on the Intelligent Methods, Systems, and Applications (IMSA):<br>
**[Download PDF](./protein_generation.pdf)**

### Instructions for training a model
Download this folder Embeddingmodel_picklefile.<br>
Use the tensorflow version 2.13 and cuda 12.8.<br>
Use any generic fasta file of protein sequences of maximum length 1024 amino acids.<br>
Run the GrantPaperMakeData.ipynb for pre-processing the data from the fasta file.<br>
Run the GrantPaperModel.ipynb to train the model.<br>
Once model is trained use the model to generate variations of any natural sequences of maximum length of 1024 amino acids.<br>

### Download Pretrained Model

Use the notebook GrantPaperModel.ipynb

The pretrained model is hosted on Hugging Face:
[![Hugging Face](https://img.shields.io/badge/Hugging%20Face-Model-yellow)](https://huggingface.co/Sayantan-95/ConvVAE1024_Condensed1500_128_k3)

### Load the Model in Python

```python
from huggingface_hub import hf_hub_download
from tensorflow import keras

# Download model file
model_path = hf_hub_download(
    repo_id="Sayantan-95/ConvVAE1024_Condensed1500_128_k3",
    filename="model.h5"
)

# Load with Keras
model = keras.models.load_model(model_path)

# Use model for sequence generation
# ...

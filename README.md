**Protein Sequence Generation with Generative AI**<br>
This project explores generative deep learning models for synthetic protein sequence generation. Using the UniProt database, we trained and evaluated several architectures—including dense and convolutional autoencoders, plus their variational forms.

Our best-performing model, a convolutional variational autoencoder, achieved the lowest reconstruction error. We found that latent space size (condensation level) strongly affects sequence identity and diversity. At 80% condensation, the model generates diverse yet biologically meaningful protein variants.

This repository includes:

Model training and generation notebooks

Preprocessing scripts

Example datasets

Instructions for reproducing results and generating new sequences

Generative AI holds strong promise for advancing protein engineering—and this repo is your starting point.<br>

**Paper**<br>
For a detailed explanation of our methods and findings, check out the full paper:<br>
**[Download PDF](./protein_generation.pdf)**

**Instructions**<br>
Download this folder Embeddingmodel_picklefile.
Use the tensorflow version 2.13 and cuda 12.8.
Use any generic fasta file of protein sequences of maximum length 1024 amino acids.
Run the GrantPaperMakeData.ipynb to generate the required matrices f-matrix and f-matrix embedded.
Run the GrantPaperModel.ipynb to train the model.
Once model is trained use the model to generate variations of any natural sequences of maximum length of 1024 amino acids.


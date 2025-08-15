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

**Instructions**
Use any generic fasta file of protein sequences of maximum length 1024 amino acids.
Run the 


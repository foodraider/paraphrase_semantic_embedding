# paraphrase_semantic_embedding

This is a baseline model for the paraphrase sentence semantic embedding extraction project.

## Introduction

The variational autoencoder (VAE) can be used to obtain the latent embedding representation of its input. Moreover, the VAE is known to enforce a regularization on the latent embedding codes, therefore smoothing the latent space. Hence, we use takes in pairs of two paraphrases and convert them to two latent representations. 
Each latent representation is then split into two segments: the semantic code and the syntax code. The model enforces a “similarity loss” on the semantic embedding codes of the two paraphrases and minimizes it. It also enforces a “difference loss” on the syntax embedding codes of the two paraphrases and maximizes it. 
Hence the model is forced to make the semantic codes of the two latent representations as similar as possible and the syntax codes of the two latent representation as different as possible. So the semantic codes should capture what are common between the two paraphrases. Moreover, since paraphrases should share similar semantics, the semantic representation should be extracted by the semantic codes through the similarity loss.


## Dataset

For the purpose of this project, we will need datasets of pairs of paraphrases. We propose two datasets: the [PPDB (the Paraphrase Database)] (http://www.cis.upenn.edu/~ccb/ppdb/) and the [Quora duplicate questions dataset] (https://data.quora.com/First-Quora-Dataset-Release-Question-Pairs)






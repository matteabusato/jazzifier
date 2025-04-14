# Jazzifier
AI Project 2025 - Berthe, Brambilla, Busato

## Genre-to-Jazz Music Conversion 

This project investigates the transformation of songs from diverse genres into jazz music using symbolic MIDI data and deep generative models. Our goal is to develop a system capable of learning and reproducing the unique harmonic, rhythmic, and improvisational characteristics of jazz from non-jazz inputs. We employ two complementary deep learning architectures: the Music Transformer, which captures long-range dependencies through self-attention mechanisms, and a Variational Autoencoder (VAE), which encodes and reconstructs musical phrases in a compressed latent space.
The process begins with curating and augmenting a diverse MIDI dataset to ensure robust training. Sequences are tokenized with special attention to rhythm, swing, and harmonic progression—key elements of jazz. The VAE is trained to reconstruct and interpolate jazz phrases, providing insights into stylistic nuances. Concurrently, the Music Transformer is trained in an autoregressive fashion to generate coherent jazz-style continuations from genre-diverse inputs.
We evaluate outputs using both quantitative metrics—such as syncopation, harmonic richness, and improvisational variation—and qualitative listening tests.

The dataset can be found at the following link: https://zenodo.org/records/8354955.
# Jazzifier
AI Project 2025 — Coline Berthe, Claudia Brambilla, Mattea Busato

## Genre-to-Jazz Music Conversion

This project explores how to transform songs from diverse genres into jazz music using symbolic MIDI data and deep generative models. Our objective is to learn and reproduce the harmonic, rhythmic, and improvisational patterns characteristic of jazz, while generalizing from non-jazz inputs.

We employ three complementary modeling approaches:

- **Recurrent Neural Networks (RNNs)**: We implement an LSTM-based RNN trained to predict the next musical event (note or chord) from fixed-length sequences. This baseline model is motivated by our exploratory data analysis, which revealed strong short-term dependencies and frequent repetitions in jazz melodies. Despite ignoring timing attributes, the RNN effectively captures local structure and provides interpretable output.

- **Variational Autoencoder (VAE)**: This architecture encodes musical phrases into a continuous latent space and reconstructs them to learn stylistic variation and phrasing. The VAE enables interpolation and creative recombination of motifs, helping us explore the expressive flexibility of jazz.

- **Music Transformer**: A Transformer model trained autoregressively to generate jazz continuations. It captures long-range dependencies and handles musical structures that span across larger time scales, such as call-and-response patterns or repeated motifs with variation.

The generation process begins with curation and augmentation of a diverse MIDI dataset. Each MIDI file is parsed and preprocessed into symbolic sequences capturing pitch, rhythm, and structure. Tokenization is customized to reflect the importance of rhythmic swing and harmonic richness.

We evaluate generated sequences with:
- **Quantitative metrics**: note density, syncopation, repetition patterns, harmonic diversity.
- **Qualitative listening tests**: musicality, genre consistency, and perceived creativity.

The dataset used in this project is publicly available at:  
🔗 [https://zenodo.org/records/8354955](https://zenodo.org/records/8354955)

## Local Simulation

To run the models locally, install the dependencies with:

```bash
pip install -r requirements.txt
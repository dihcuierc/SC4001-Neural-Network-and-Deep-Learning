# Small Data, Big Impact: Enhancing Sentiment Classification with Variational Autoencoders

## Overview

This project explores the use of **Variational Autoencoders (VAEs)** for augmenting small datasets to enhance performance in **sentiment classification tasks**. It evaluates the effectiveness of VAE-generated data on improving model generalization and accuracy for models like BERT, GPT-2, and LSTM in low-resource settings.

## Features

- **Data Augmentation:** Utilizes VAEs to generate synthetic data, addressing data scarcity issues in sentiment analysis.
- **Model Comparisons:** Benchmarks the performance of encoder-only (BERT), decoder-only (GPT-2), and LSTM-based sentiment classifiers.
- **Small Dataset Focus:** Demonstrates the impact of data augmentation on datasets as small as 100 samples.
- **Performance Metrics:** Evaluates models using accuracy, precision, recall, F1-score, and cross-entropy loss.

## Dataset

- **IMDB Dataset:** A small subset of 100 labeled movie reviews used as the base dataset.
- **Rotten Tomatoes Dataset:** Training of VAE
- **VAE-Augmented Datasets:** Expanded datasets of 200 and 500 samples generated via VAE augmentation.

## Methodology

1. **Variational Autoencoder (VAE):**
   - Encoder: Built on **DistilBERT**, capturing latent semantic information.
   - Decoder: Constructs synthetic sentences from latent vectors using a **Gated Recurrent Unit (GRU)**.
2. **Sentiment Classification Pipeline:**
   - Augmented datasets are used to fine-tune sentiment classifiers.
   - Classifiers include BERT, GPT-2, and LSTM.

## Results

- **BERT:** Consistently outperformed other models across datasets, with significant improvements in validation accuracy and F1-score.
- **GPT-2 and LSTM:** Showed performance gains with augmentation but were less consistent than BERT.
- **VAE Augmentation:** Improved model performance but showed diminishing returns with increasing synthetic data.

## Limitations

- Computational constraints limited the use of larger models like GPT-2.
- Some synthetic samples lacked coherence, highlighting areas for improvement in VAE training.

## Future Work

- Explore complementary data augmentation methods for greater diversity in synthetic data.
- Optimize VAE architectures to balance coherence and variability.
- Extend experiments to larger datasets and additional NLP tasks.

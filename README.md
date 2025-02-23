# URM: Wavelet-Based Tokenization-Free Text Processing

## Overview

This project implements **URM** (Unique Relational Model), a novel neural network architecture designed to process raw text data without traditional tokenization. Inspired by advancements in efficient sequence modeling—such as the Fourier Transform approach in "FNet: Mixing Tokens with Fourier Transforms" ([arXiv:2105.03824](https://arxiv.org/abs/2105.03824))—URM combines **learnable wavelet transforms**, **convolutional modulation**, and **graph convolutional networks (GCNs)** to predict next characters in a sequence. The model is trained and tested on the Tiny Shakespeare dataset, demonstrating a fully tokenization-free pipeline.

Unlike conventional NLP models that rely on tokenized inputs (e.g., words or subwords), URM treats text as a raw signal of character indices. This approach leverages wavelet transforms to extract multi-scale features directly from the signal, offering a fresh perspective on text processing that avoids predefined vocabulary constraints.

## Key Features

- **Tokenization-Free**: Processes raw text as a continuous signal of character indices, eliminating the need for a tokenizer or vocabulary.
- **Learnable Wavelet Layer**: Applies continuous wavelet transforms (CWT) with trainable scales to capture multi-scale patterns in the input signal.
- **Convolutional Modulation**: Refines wavelet features using 1D convolutions for enhanced representation.
- **Graph Convolutional Networks (GCNs)**: Incorporates structural relationships via dependency graphs (currently simple linear chains).
- **Next-Character Prediction**: Trained to predict the next character in a sequence, demonstrated on Tiny Shakespeare.
- **Inspired by FNet**: Adapts the idea of replacing attention with transforms (wavelets here instead of Fourier) for efficient sequence modeling.

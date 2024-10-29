# TimbreTransfer

This is the code repository for the paper Instrumental Timbre Transfer based on Disentangled Representation of Timbre and Pitch. 

## Abstract

In order to investigate the possibility of effective representation for pitch and timbre, this paper presents a novel framework for multiple-to-multiple instrumental timbre transfer using a beta-variational autoencoder (β-VAE). This framework separates and manipulates the timbral and pitch characteristics of musical instruments without requiring annotated data. Through the dual-encoder system, it effectively disentangles the timbre and pitch, enabling the transfer of timbral characteristics across different musical notes and instruments while preserving the original pitch information. This also implicitly creates a loss function for timbre in the system. Training with the dataset generated from MIDI files encompassing a diverse range of timbres, this framework shows impressive generalization ability that can distinguish various unseen timbres. The results demonstrate superior performance in timbre transfer compared to up-to-the-date existing methods, offering potential applications in music production and automatic music transcription systems where timbral consistency is considered as crucial.

## Usage

The training and inference code are provided in:
[![Run in Colab](https://colab.research.google.com/drive/1pBT4P_FWldxADBgfzgM3hgVUdX9QArPP?usp=sharing)


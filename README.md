# Hugging Face and Gradio Tutorial

This repository contains a short tutorial demonstrating how to build interactive applications using **Gradio** and **Hugging Face Transformers**. The goal of the tutorial is to introduce the basics of creating Gradio apps with common interface components and to show how pretrained deep learning models can be easily integrated using Hugging Face’s `pipeline()` API.

The project is implemented as a single Jupyter notebook and is intended as a simple, instructional example rather than a production system.

---

## Tutorial Overview

The tutorial is divided into two main parts.

### 1. Building a Gradio App (Layout and Components)

The first part of the tutorial discusses the fundamentals of building a Gradio application using:
- `Blocks` for custom layouts
- `Row` and `Column` for structuring the interface
- Common components such as images, text inputs, sliders, buttons, and live outputs
- Event handling using `.click()` and `.change()`

These concepts are demonstrated through a creative Gradio app called **Poster Critic Studio**. In this app, users can upload an image, select a mood, and adjust sliders to generate a movie-poster-style tagline, a critic score (0–100), and a simple color/brightness/contrast summary derived from the image. The app uses lightweight image statistics and custom logic to produce interactive and creative outputs.

---

### 2. Hugging Face Transformers and Pipelines in Gradio

The second part of the tutorial demonstrates how to use the Hugging Face `transformers` library inside a Gradio app. It uses the `pipeline("sentiment-analysis")` interface, which provides access to a pretrained sentiment classification model with only a few lines of code.

This pipeline is demonstrated in two ways:
- A standalone **Sentiment Tool** tab where users can input any text and receive a sentiment label and confidence score
- Automatic sentiment analysis of the tagline generated in the Poster Critic Studio app

This section highlights how pretrained models can be integrated into interactive applications without any model training or fine-tuning.

---

## Hugging Face Model Description

The tutorial uses Hugging Face’s `pipeline()` abstraction for sentiment analysis. The pipeline automatically downloads a publicly available pretrained model (a DistilBERT model fine-tuned on the SST-2 dataset) at runtime. No model weights are stored in this repository, and no authentication is required, as all models used are publicly available.

---



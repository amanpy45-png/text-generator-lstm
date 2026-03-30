**Text Generator with LSTM**

This project is a text generation model built using TensorFlow and Keras that can generate quotes. It uses a Recurrent Neural Network (LSTM) to predict the next word in a sequence based on a set of quotes.
---


Features:

Generates quotes inspired by Naruto anime/manga.
Uses LSTM for sequence prediction.
Trained on a small set of motivational and philosophical quotes.
Can generate multiple words continuously to form meaningful sentences.


---

## Table of Contents

* [Overview](#overview)
* [Dataset](#dataset)
* [Installation](#installation)
* [Usage](#usage)
* [Model Architecture](#model-architecture)
* [How It Works](#how-it-works)
* [Example Output](#example-output)
* [License](#license)

---

## Overview

This project demonstrates how to build a word-level text generator using a **Recurrent Neural Network (RNN)** with **Long Short-Term Memory (LSTM)** layers. The model learns patterns in text sequences and predicts the next word based on previous words, allowing it to generate new text in a similar style.

---

## Dataset

The model is trained on a collection of motivational quotes:

```
Hard work is worthless for those that don’t believe in themselves
I’m not gonna run away, I never go back on my word that’s my ninja way
When people are protecting something truly precious to them they can become as strong as they need to be
...
Protecting others is what gives your life meaning
```

> Note: The dataset is embedded directly in the Python code as a multi-line string. You can expand this dataset with more quotes for better results.

---

## Installation

1. Clone this repository:

```bash
git clone https://github.com/your-username/quote-text-generator.git
cd quote-text-generator
```

2. Install required Python packages:

```bash
pip install tensorflow numpy
```

---

## Usage

1. Run the training script:

```bash
next-word-pred-lstm.ipynb
```

2. Generate new quotes by providing a seed word:

```python
text = "Failing"
# The model will generate a sequence of words based on the seed text
```

3. You can modify the number of generated words by changing the loop:

```python
for i in range(10):
    ...
```

---

## Model Architecture

The model uses the following layers:

1. **Embedding Layer**

   * Converts word indices into dense vectors
   * Input dimension: vocabulary size (136)
   * Output dimension: 100

2. **LSTM Layer**

   * 150 LSTM units
   * Captures temporal relationships between words

3. **Dense Layer**

   * Output layer with softmax activation
   * Predicts the next word in the sequence

---

## How It Works

1. **Tokenization** – Converts words into integer sequences.
2. **Sequence Creation** – Creates input sequences of increasing length for training.
3. **Padding** – Pads sequences to the same length to feed into the LSTM.
4. **One-Hot Encoding** – Converts output words into one-hot vectors for classification.
5. **Model Training** – Uses categorical cross-entropy loss and Adam optimizer.
6. **Text Generation** – Predicts the next word iteratively based on the previous sequence.

---

## Example Output

If the seed text is `"Failing"`, the model might generate something like:

```
Failing doesn’t give you a reason to give up as long as you believe

```

## License

This project is licensed under the MIT License.



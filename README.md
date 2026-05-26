# Bigram Language Model for Language Identification

## Overview

This project implements a **Bigram Language Model** using Python and NLTK to identify languages based on text probability calculations.
The model is trained using English, French, and Italian datasets and uses **Laplace (Add-One) Smoothing** to handle unseen word pairs.

The project was developed in **Google Colab** with datasets stored in **Google Drive**.

---

## Features

* Text preprocessing and tokenization using NLTK
* Bigram language model training
* Add-One (Laplace) smoothing
* Log probability calculation for sentences
* Language identification using probabilistic modeling
* Support for multiple languages

---

## Technologies Used

* Python
* NLTK
* Scikit-learn
* Google Colab
* Google Drive Integration

---

## Project Structure

```bash
.
├── Prg2_BigramLanguageModel.ipynb
├── README.md
├── LangId.train.English
├── LangId.train.French
├── LangId.train.Italian
└── LangId.test
```

---

## How the Model Works

### 1. Preprocessing

* Converts text into lowercase
* Tokenizes sentences into words
* Removes empty lines

Example:

```python
Hello World!
```

Becomes:

```python
['hello', 'world', '!']
```

---

### 2. Bigram Model Training

The model learns:

* **Unigram counts** → frequency of single words
* **Bigram counts** → frequency of word pairs

Sentence boundary markers are added:

```text
<s> hello world </s>
```

---

### 3. Probability Calculation

The probability of a word occurring after another word is calculated using:

P(w_2\mid w_1)=\frac{\mathrm{count}(w_1,w_2)+1}{\mathrm{count}(w_1)+V}

Where:

* ( count(w_1, w_2) ) = frequency of the bigram
* ( count(w_1) ) = frequency of the first word
* ( V ) = vocabulary size

---

## Installation

### Clone the Repository

```bash
git clone https://github.com/your-username/bigram-language-model.git
cd bigram-language-model
```

### Install Required Libraries

```bash
pip install nltk scikit-learn
```

---

## Dataset Setup

Place the following files inside your Google Drive folder:

```bash
My Drive/Lab Sessions/
```

Required files:

* `LangId.train.English`
* `LangId.train.French`
* `LangId.train.Italian`
* `LangId.test`

---

## Running the Project

Open the notebook in Google Colab and run all cells.

The notebook will:

1. Mount Google Drive
2. Load datasets
3. Preprocess text
4. Train the bigram models
5. Calculate probabilities
6. Predict the language of test sentences

---

## Example Workflow

### Input Sentence

```text
Bonjour comment allez vous
```

### Model Prediction

```text
Predicted Language: French
```

---

## Key Concepts Used

* Natural Language Processing (NLP)
* Statistical Language Modeling
* Bigram Probabilities
* Laplace Smoothing
* Log Probability Computation

---

## Future Improvements

* Add trigram language models
* Improve preprocessing
* Add support for more languages
* Create a web interface
* Use deep learning approaches for comparison

---

## Author

**Akash Abeywickrame**

Undergraduate Student | Software Engineering & AI Enthusiast

---

## License

This project is created for educational and research purposes.

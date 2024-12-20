# Smoothing Techniques in NL

## Overview

This repository implements various **smoothing techniques** for n-gram language models. Smoothing is a crucial step in natural language processing (NLP) and text generation, especially when working with small or sparse datasets. The techniques included are:

1. **Laplace Smoothing** (Additive Smoothing with \( k = 1 \))
2. **Additive Smoothing** (with arbitrary \( k \))
3. **Interpolated Smoothing** (combining Unigrams and Bigrams)

Each technique helps improve the estimation of probabilities for unseen n-grams, ensuring a more robust language model. These techniques are applied to a simple text corpus to compute word and n-gram probabilities.

## Features

- **Laplace Smoothing**: Applies the classic additive smoothing technique (with \( k = 1 \)) to adjust word probabilities by adding 1 to the counts, ensuring no zero probabilities.
  
- **Additive Smoothing**: Extends Laplace Smoothing to work with a customizable constant \( k \). This allows you to control the degree of smoothing applied to the model, which can be helpful for different datasets.

- **Interpolated Smoothing**: Combines the probability distributions of unigrams and bigrams using interpolation weights (\( \lambda_1 \) and \( \lambda_2 \)) to balance the contributions of smaller and larger n-grams for more accurate probability estimation.

- **Tokenizer and N-gram Generator**: Uses `nltk` for tokenization and custom functions for generating n-grams (unigrams, bigrams) and their respective probability distributions.

- **Probability Calculation**: Computes the smoothed probabilities for individual words (Laplace and Additive) and for n-grams (Interpolated), displaying the results for further analysis.

## Agile Features

1. **Modular Design**: The code is structured in a modular way, making it easy to swap or extend smoothing techniques. You can experiment with additional smoothing methods, such as **Good-Turing** or **Kneser-Ney** smoothing, by adding new functions or modifying existing ones.

2. **Parameter Tuning**: The repository allows easy experimentation with key parameters like \( k \) (for additive smoothing) and the interpolation coefficients (\( \lambda_1 \) and \( \lambda_2 \) for interpolated smoothing). This flexibility supports the agile approach of iterative testing and improvement.

3. **Scalability**: Although the current implementation works with a small sample corpus, the design can be easily scaled to work with larger corpora or datasets. This allows for quick iteration and testing with real-world language data.

4. **Documentation and Examples**: The repository provides clear code with inline comments and printed outputs for every step. This makes it easy for collaborators to understand and improve the code, supporting the agile principle of continuous collaboration and feedback.

## Conclusion

This repository demonstrates essential smoothing techniques for n-gram language models. By applying **Laplace**, **Additive**, and **Interpolated Smoothing**, the repository provides a strong foundation for building more sophisticated language models. The code is modular, flexible, and easy to adapt, offering great potential for further improvements, including the addition of new smoothing methods or enhancements for scalability and performance.

The repository serves as a valuable resource for anyone working with NLP tasks like text generation, speech recognition, or machine translation, where handling unseen data and sparse events is critical.

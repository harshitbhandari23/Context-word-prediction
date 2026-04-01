# 🧠 NLP Middle Word Prediction using N-grams

## 📌 Project Overview

This project builds a simple NLP-based model that predicts a **missing middle word** given its left and right context using an **N-gram approach**.

Example:

```
Input:  "in the ___ of the"
Output: "middle word prediction"
```

The model uses frequency-based probability from a text corpus.

---

## 🚀 Features

* Text preprocessing using regex
* N-gram generation
* Frequency-based probability estimation
* Context-based word prediction
* Simple and interpretable logic (no deep learning)

---

## 🛠️ Technologies Used

* Python
* Pandas
* Regular Expressions (re)
* Collections (Counter)

---

## 📂 Dataset

* Input file: `big.txt`
* Should contain large text corpus

Upload file using:

```python
from google.colab import files
files.upload()
```

---

## ⚙️ How It Works

### 1. Text Preprocessing

* Convert text to lowercase
* Extract words using regex

### 2. N-gram Generation

* Creates sequences of words (default: 5-grams)
* Example:

```
"this is a very good day"
```

### 3. Context Splitting

From each n-gram:

* Left context
* Right context
* Middle word (target)

Example:

```
Left: "this is"
Right: "good day"
Output: "a"
```

### 4. Frequency Calculation

* Counts occurrences of each pattern
* Stores probability information

### 5. Prediction

* Matches left + right context
* Returns most frequent middle word(s)

---

## 📊 Example Usage

```python
inp = 'in the_of the'
left, right = inp.split('_')

predict(left, right)
```

Output:

```
['middle_word']
```

---

## 🧪 Functions Explained

### 🔹 get_pair(words, n)

Generates n-grams from word list.

### 🔹 get_prob(pair)

Creates probability distribution:

* Left context
* Right context
* Middle word
* Frequency

### 🔹 predict(left, right)

Returns most probable middle word.

---

## ⚠️ Limitations

* No semantic understanding
* Works only on seen patterns
* Cannot generalize like neural networks

---

## 🔥 Future Improvements

* Replace with Neural Networks (RNN/LSTM)
* Use Embedding layer for better representation
* Add smoothing techniques
* Use larger datasets

---

## 💡 Learning Outcome

* Understanding of N-grams
* Basics of language modeling
* Transition from statistical NLP → Deep Learning

---

## 👨‍💻 Author

Developed as part of NLP learning journey.

---

## ⭐ If you like this project

Give it a star on GitHub!

# Generative-Text-Model

*COMPANY*: CODTECH IT SOLUTUIONS

*NAME*: MAKWANA SAKSHI M

*INTERN ID*: C0DF93

*DOMAIN*: ARTIFICIAL INTELLIGENCE MARKUP LANGUAGE

*DURATION*: 4 WEEKS

*MENTOR*: NEELA SANTHOSH


# 🤖 Generative Text Model using Optimized LSTM

This project presents an **optimized generative text model** utilizing **LSTM (Long Short-Term Memory)** networks, trained on **Medium article titles**.
It is designed to **predict and generate text sequences** with a focus on **efficiency, reduced computational load, and improved handling of sequence generation edge cases**.


## 📝 Overview:
* **Task:** Next-word text generation.
* **Dataset:** Medium article titles (`medium_data.csv`).
* **Optimizations:**

  * Controlled **vocabulary size (`5000`)**.
  * Simplified yet effective **LSTM architecture (2 layers, 100 units each)**.
  * Improved **text generation function** with robust handling of sequence shapes and predictions.


## 📂 Dataset:
Ensure you have a **CSV file with a `title` column**:

| title                               |
| ----------------------------------- |
| Artificial intelligence is evolving |
| College life is transformative      |
| How to boost productivity           |

Save this file as:

```
/content/medium_data.csv
```


## ⚙ Installation & Setup:

1. **Clone the Repository:**
   ```bash
   git clone https://github.com/yourusername/generative-text-optimized-lstm.git
   cd generative-text-optimized-lstm
   ```

2. **Install Required Libraries:**
   ```bash
   pip install numpy pandas tensorflow matplotlib
   ```


## 🔧 Working:

### Step 1: Data Preprocessing
* Loads and cleans the dataset.
* Applies tokenization using **Keras Tokenizer (vocabulary size: 5000, OOV token enabled)**.
* Prepares input sequences and labels for supervised training.

### Step 2: Model Building & Training
* Embedding layer converts tokens into dense vectors.
* Stacked **LSTM layers with Dropout regularization**.
* **Softmax output layer** predicts next-word probabilities.
* Model is trained using **categorical cross-entropy** over 15 epochs.

### Step 3: Accuracy Visualization
* Training accuracy is plotted over epochs.

### Step 4: Text Generation
* User provides a **seed text**.
* The model predicts the **next N words**, generating coherent text.


## 💻 How to Run:
Run the main script:

```bash
python train_and_generate.py
```

Ensure your dataset path in the script matches:

```python
medium_data = pd.read_csv('/content/medium_data.csv')
```


## 🎯 Example Usage & Output:
```python
print(generate_text("Artificial intelligence", 5))
```

**Sample Output:**
```
Artificial intelligence is the future of technology and
```

```python
print(generate_text("College life is", 5))
```

**Sample Output:**
```
College life is the best way to explore opportunities
```

> Output may vary based on dataset content and training state.


## ✨ Customization Options:
* **Vocabulary Size:** Adjust `num_words` in the tokenizer.
* **Model Complexity:** Modify number of LSTM units, Dropout rates, or add more layers.
* **Generation Length:** Change `next_words` parameter in `generate_text()` function.


## 🛠 Model Architecture:

```plaintext
Embedding Layer (64 dimensions)
│
├── LSTM (100 units, return_sequences=True)
│
├── Dropout (0.2)
│
├── LSTM (100 units)
│
└── Dense (Softmax over vocabulary size)
```


## 🔮 Future Enhancements:
* Integrate **Beam Search or Top-K Sampling**.
* Explore **Attention Mechanisms**.
* Use **GRU or Transformer-based models**.
* Train on **diverse text datasets** for improved generalization.


## 📄 License:
Licensed under the **MIT License**.
Free for both personal and commercial use.


## 🎯 Output:
![Image](https://github.com/user-attachments/assets/f2fffafb-579d-4af9-98ca-d4cd71314547)

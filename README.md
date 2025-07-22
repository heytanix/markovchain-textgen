# Text Generation Using First-Order Markov Chains

## Introduction
This project demonstrates a simple method for procedural text generation using a **first-order Markov chain**. A Markov chain is a probabilistic model where the likelihood of a future state depends only on the current state. In the context of natural language, we treat each word as a state, and the model learns the probability of which word will come next based on the current word.

The model is trained on a small, self-contained corpus of text. The generated output mimics the style and vocabulary of this source text.

## 🫡 You can help me by Donating
[![BuyMeACoffee](https://img.shields.io/badge/Buy%20Me%20a%20Coffee-ffdd00?style=for-the-badge&logo=buy-me-a-coffee&logoColor=black)](https://buymeacoffee.com/heytanix)

### Corpus Overview:
-   **Source**: A short, descriptive paragraph about a sunset over a lake.
-   **Content**: The text describes a serene natural scene, establishing a calm and picturesque tone.
-   **Structure**: The model analyzes word-to-word transitions within this text.

**Objective**:
The goal is to build a simple, functional text generator from scratch that can create new sentences based on the statistical patterns learned from a given corpus.

## Techniques & Libraries Used
The project is built entirely in Python using standard libraries, emphasizing the core logic of the algorithm.

1.  **Python 3**: The core programming language.
2.  **Jupyter Notebook**: For interactive development and demonstration.
3.  **`random` library**: Used to randomly select the next word in the chain from a list of possible followers.
4.  **`collections.defaultdict`**: A specialized dictionary used to efficiently build the Markov chain model by providing a default value (an empty list) for new words.

## Project Workflow
### Step 1: Defining the Corpus
A sample paragraph is defined in the `building_text` variable. This text serves as the training data for our model.

### Step 2: Building the Markov Chain Model
-   The `build_markov_chain` function processes the corpus.
-   It tokenizes the text into words and iterates through them to build a dictionary.
-   Each key in the dictionary is a word, and its value is a list of all words that have directly followed it in the corpus.

### Step 3: Generating Text
-   The `generate_text` function uses the completed Markov model to create new sentences.
-   It starts with a `start_word` and iteratively looks up the current word in the model.
-   It then uses `random.choice()` to pick the next word from the list of followers and appends it to the output.
-   This process repeats until the desired number of words is generated.

### Conclusion
This project successfully demonstrates the implementation of a basic text generator using a first-order Markov chain. The model effectively captures the immediate word-to-word relationships from the source text to create new, short sequences.

The primary limitation is the lack of long-term context; since the model only considers the single preceding word, the generated sentences can lose coherence over longer lengths. However, it serves as an excellent introduction to the principles of probabilistic language models.
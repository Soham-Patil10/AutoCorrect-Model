# Autocorrect Model

### Overview
This project implements an autocorrect system using Python. It suggests corrections for misspelled words based on a predefined vocabulary and word frequency data. The system uses edit distance calculations to generate possible corrections and selects the most probable word based on word probabilities.

### Features
- **Edit Distance Calculation**: Generates candidate words within an edit distance of 1 or 2 from the input word.
- **Vocabulary Matching**: Matches candidate words against a predefined vocabulary sourced from an English dictionary CSV file.
- **Probabilistic Correction**: Selects the most likely correct word based on word frequency probabilities derived from corpus data.
### Installation
1. Clone this repository:
    ```bash
    git clone https://github.com/UllekhPatel/Autocorrect-Model.git
    cd Autocorrect-Model
    ```

2. Install dependencies:
    ```bash
    pip install numpy pandas
    ```

3. Add the English dictionary CSV file in the appropriate directory, or use the link provided below to download it.

### Usage
- Run the Jupyter notebook:
    ```bash
    jupyter notebook autocorrect.ipynb
    ```
- Follow the notebook instructions to input a word and receive autocorrect suggestions.

### Functions
- **edit1(word)**: Generates all possible edits that are one edit distance away from the input word.
- **edit2(word)**: Generates all possible edits that are two edits away.
- **correct_spelling(word, vocabulary, word_probabilities)**: Suggests corrections for the input word based on the provided vocabulary and word probabilities.

## Example

When you input a word like `"botes"`, the system may suggest corrections like:

```plaintext
[('notes', 7.220129721664e-05), ('bones', 2.4067099072213332e-05), ('bote', 1.2033549536106666e-05), ('boxes', 1.2033549536106666e-05), ('votes', 1.2033549536106666e-05)]
```

The system will then select the most probable correction, for example, `"notes"`.

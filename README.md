# SemanticFilter

## Overview
**SemanticFilter** is an NLP toolkit for filtering and classifying text documents based on semantic similarity. Using multiple models, this tool evaluates and categorizes documents, identifying those that meet a given similarity threshold.

This project is designed for applications in **semantic text filtering**, **document classification**, and **text preprocessing** for NLP tasks. 

## Features
- Supports multi-model similarity checks to validate results
- Allows customizable similarity threshold and element percentage for filtering
- Provides an easy-to-use API for integration into larger NLP pipelines

## Table of Contents
1. [Installation](#installation)
2. [Usage](#usage)
3. [Example](#example)
4. [Project Structure](#project-structure)
5. [Contributing](#contributing)
6. [License](#license)

## Installation
1. **Clone the repository**:
    ```bash
    git clone https://github.com/YourUsername/TextSimilarityFilter.git
    cd TextSimilarityFilter
    ```

2. **Install dependencies**:
    This project relies on several libraries including `nltk`, `spacy`, and optionally, `transformers` for advanced models.
    ```bash
    pip install -r requirements.txt
    ```
3. **Download NLP Models**:
   ```bash
   python -m spacy download en_core_web_md
   ```

## Usage
The main function in this package is `filter_text`, which classifies text based on similarity criteria. Adjust `percentage_elements` and `percentage_max_value` to set filtering parameters.

### Sample Code
```python
from TextSimilarityFilter import filtering
from sentence_transformers import SentenceTransformer

# Example inputs
text = ["Document 1 content", "Document 2 content", ...]
query = "Your reference query"

# Load model
model = SentenceTransformer("all-MiniLM-L6-v2")

# Run filtering
results = filtering(text, model, query, percentage_elements=10, percentage_max_value=80)
print(results)
```

## Example
Here's an example showing how `TextSimilarityFilter` can be used to filter documents in a Pandas DataFrame:

```python
import pandas as pd
from TextSimilarityFilter import filtering
from sentence_transformers import SentenceTransformer

# Load your data
data = pd.DataFrame({"documents": ["Text 1", "Text 2", ...]})

# Define query and initialize model
query = "Relevant topic for filtering"
model = SentenceTransformer("all-MiniLM-L6-v2")

# Apply filtering
data["filtered"] = data["documents"].apply(lambda x: filtering(x, model, query, percentage_elements=10, percentage_max_value=80))
```

## Project Structure
- **TextSimilarityFilter/**: Core modules
  - **filtering.py**: Main filtering and similarity checking functions
  - **utils.py**: Utility functions for text preprocessing
- **tests/**: Test cases to validate functionality
- **README.md**: Project overview and usage instructions

## Contributing
Contributions are welcome! If you'd like to contribute:
1. Fork this repository
2. Create a new branch for your feature (`git checkout -b feature-name`)
3. Make your changes
4. Submit a pull request

## License
This project is licensed under the MIT License.

---

This README format provides users with an easy way to understand, set up, and use your project. Make sure to update the instructions and descriptions to match your exact project details.

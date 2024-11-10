# Article Collection Filtering and Classification

This project provides a solution to streamline the early-stage collection of scientific articles by filtering and classifying articles based on their relevance to specified research topics. The solution applies natural language processing (NLP) techniques to identify and categorize articles with relevant keywords, thus minimizing the manual effort in reviewing a large number of documents.

## Project Overview

This project aims to:
1. **Filter Articles by Relevance**: Using heuristic and similarity-based approaches, this solution determines whether articles meet relevance criteria based on specific keywords in the fields of virology and epidemiology.
2. **Classify Articles by Method**: For articles deemed relevant, the solution categorizes them according to the research methodology described in the abstract, specifically focusing on:
    - Text Mining
    - Computer Vision
    - Both Text Mining and Computer Vision
    - Other methods

## Key Features

1. **Preprocessing**: Includes tokenization, stopword removal, stemming, lemmatization, and special character removal.
2. **Similarity-based Filtering**: Uses lightweight models (Sentence Transformer models) to calculate similarity scores between query terms and article abstracts, ensuring efficient operation on personal devices or free platforms.
3. **Article Classification**: Based on the average similarity of each article to key terms, articles are classified into categories for easier analysis.

## Requirements

The project relies on the following libraries:
- `pandas`
- `numpy`
- `scikit-learn`
- `matplotlib`
- `seaborn`
- `nltk`
- `spacy`
- `torch`
- `sentence_transformers`

Install the dependencies using:
```bash
pip install pandas numpy scikit-learn matplotlib seaborn nltk spacy torch sentence-transformers
```

## Usage

1. **Data Loading and Processing**: Supply a CSV file containing article titles and abstracts. The script preprocesses the text data and merges the title and abstract into a single text column for analysis.
2. **Keyword Filtering**: Customize the `query_terms` variable to adjust the keywords for relevance detection based on the research topic.
3. **Method Classification**: Adjust thresholds in `assign_method_labels` if needed to refine classification into text mining, computer vision, both, or other methods.

### Example

To run the filtering and classification, use the `main()` function:
```python
file_path = "path_to_your_file.csv"
processed_data = main(file_path)
processed_data.to_csv("processed_data.csv", index=False)
```

After filtering, the solution visualizes and saves the output, providing insight into the distribution of relevant articles.

### Visualization
The script generates visualizations to assess:
1. The number of filtered articles
2. Similarity distributions for text mining and computer vision methods
3. Correlations between the similarity measures

## Code Structure

- **Data Loading and Preprocessing**: `load_data`, `fill_na`, `merge_columns`, `preprocess_text`
- **Filtering Functions**: `filter_text`, `polishing`
- **Classification Functions**: `calculate_avg_similarity`, `assign_method_labels`

## Evaluation Criteria

- **Clarity of README**: This README provides a clear overview and usage guide, allowing users to quickly understand the purpose and operation of the solution.
- **Simplicity and Code Cleanliness**: The solution uses lightweight NLP models, ensuring suitability for personal devices. Heuristic filtering and simple model-based approaches avoid the need for complex, resource-intensive language models.

---

This README introduces your solution, highlights its simplicity, and offers a concise guide to the code’s purpose and usage, ensuring easy comprehension for your interviewer or any user. Let me know if you’d like more customization or additional information.


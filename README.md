# Semantic NLP Filtering for Deep Learning Papers in Virology/Epidemiology

## Project Overview
The goal of this project is to filter and classify academic papers from a dataset created through keyword-based searches on PubMed. The dataset contains 11,450 records and includes papers related to virology and epidemiology. This project utilizes Natural Language Processing (NLP) techniques to identify papers that implement deep learning neural network-based solutions in these fields. For the papers that meet the criteria, we classify them based on the type of method used: ["text mining", "computer vision", "both", "other"].

## Dataset
The dataset is available in CSV format and includes a header row with multiple records. Each record contains metadata for individual academic papers. The list of keywords used for the initial search can be accessed [here]().

- **Number of records**: 11,450
- **Columns**: Title, Abstract, Authors, Journal, Keywords, and other relevant metadata.

You can download the dataset from the [Virology AI Papers Repository]().

## Approach

### 1. **NLP Filtering Technique**
For filtering papers, we have implemented **semantic NLP techniques** to identify papers that use deep learning approaches in virology and epidemiology. This technique goes beyond simple keyword matching and allows us to:
- **Contextual understanding**: It recognizes context and relationships between words, reducing false positives and negatives that might occur with traditional keyword-based filtering.
- **Model used**: A pre-trained **BERT (Bidirectional Encoder Representations from Transformers)** model fine-tuned on a custom corpus related to virology, epidemiology, and deep learning papers.

By applying semantic NLP techniques, we can better understand the content of the papers and filter them based on their relevance to the task, rather than relying solely on static keywords.

### 2. **Paper Classification**
Once relevant papers are identified, they are classified into the following categories based on the method they describe:
- **Text Mining**: Papers using deep learning for text processing tasks (e.g., sentiment analysis, document classification).
- **Computer Vision**: Papers using deep learning for image analysis tasks (e.g., medical imaging, image classification).
- **Both**: Papers that use deep learning methods in both text mining and computer vision.
- **Other**: Papers using deep learning methods that don't fit into the other categories.


### 3. **Method Extraction**
For each relevant paper, the specific deep learning method used (e.g., Convolutional Neural Networks, Recurrent Neural Networks, etc.) is extracted from the abstract and/or title. This method is reported alongside the paper's classification.

## Results

- **Filtered Papers**: After applying the NLP filtering technique, we identified [X] (out of 11,450) relevant papers from the dataset.
- **Classification Breakdown**:
  - Text Mining: [X%]
  - Computer Vision: [X%]
  - Both: [X%]
  - Other: [X%]


## Installation

1. **Clone the repository**:
   ```bash
   git clone https://github.com/username/projectname.git
   ```

2. **Install dependencies**:
   The project requires Python 3.x and several libraries. You can install them using:
   ```bash
   pip install -r requirements.txt
   ```

3. **Prepare the dataset**:
   Download the dataset and place it in the `data/` directory.

4. **Run the filtering and classification**:
   After setting up, you can run the code using the following command:
   ```bash
   python filter_and_classify.py --dataset data/papers.csv --output results.csv
   ```

   This will filter and classify the papers, outputting the results into a CSV file.

## Code Explanation

### 1. **filter_and_classify.py**
   - **Input**: A CSV file containing the academic papers dataset.
   - **Processing**:
     - Filters the papers using semantic NLP techniques.
     - Classifies each paper based on the type of deep learning method used.
     - Extracts the deep learning method (e.g., CNN, RNN).
   - **Output**: A CSV file with classified papers and their corresponding methods.

### 2. **nlp_filter.py**
   - Implements the BERT-based semantic filtering.
   - This script uses the pre-trained BERT model, fine-tuned for the domain-specific dataset to filter out irrelevant papers.

## Why NLP-based Filtering?

Traditional keyword-based filtering has its limitations in dealing with variations in terminology and context. Semantic NLP techniques, such as BERT, offer the following advantages:
- **Contextual understanding**: BERT can understand the meaning of words in context, thus identifying papers that mention deep learning methods but use different terminology.
- **Flexibility**: The model can adapt to papers with various writing styles, technical language, and abstract terminology, making it more robust than keyword matching.

## Future Work
- Extend the filtering model to include additional techniques such as **Named Entity Recognition (NER)** to identify specific neural network architectures or methods mentioned in the papers.
- Integrate additional classification categories to cover other deep learning applications in virology and epidemiology.

## Contributing
Contributions are welcome! If you'd like to suggest improvements or add new features, please:
1. Fork the repository.
2. Create a new branch for your changes.
3. Submit a pull request with a description of your changes.

## License
This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Contact Information
For questions or feedback, feel free to reach out to javahedi@gmail.com.

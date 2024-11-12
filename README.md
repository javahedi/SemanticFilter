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


## Jupyter Notebook: `nlp-project.ipynb`

This project includes a Jupyter notebook, `nlp-project.ipynb`, which contains all the necessary code for:
- **Loading the dataset** and preprocessing it.
- **Filtering papers** using semantic NLP techniques (BERT).
- **Classifying papers** into one of the predefined categories.
- **Extracting deep learning methods** used in each paper.

### How to Run the Jupyter Notebook:
1. **Clone the Repository:**
 ```bash
   git clone https://github.com/username/projectname.git
  ```
2. **Install Dependencies**: Install the required libraries using:
  ```bash
    pip install -r requirements.txt
  ```
3. **Launch Jupyter Notebook**: Open the notebook by running:
  ```bash
    jupyter notebook nlp-project.ipynb
  ```

4. *Run the Cells**:
  - Follow the instructions within the notebook to load the dataset, apply the NLP filter, and classify the papers.
  - The notebook will guide you through the steps for extracting the deep learning methods used in each paper.


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

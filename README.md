# Emotion Detection in Text

A deep-learning project that uses a **Bidirectional Long Short-Term Memory (BiLSTM)** network and TensorFlow to classify text into three sentiment categories: **Positive, Negative, and Neutral**.

The model is trained on a custom dataset of comments collected from YouTube and Twitter. The project explores how recurrent neural networks can learn contextual patterns in text and distinguish between different sentiment polarities.

> **Note:** Despite the repository name, the current implementation performs three-class sentiment classification rather than emotion-specific classification.

## Overview

Understanding sentiment in online comments can help identify opinions and attitudes expressed in text. This project applies deep learning to classify comments according to their overall sentiment polarity.

The implementation uses a BiLSTM architecture to process tokenized text and learn contextual relationships between words. Model performance is evaluated using accuracy, loss, precision, recall, and F1-score.

### Key Features

- Three-class sentiment classification: Positive, Negative, and Neutral
- Bidirectional LSTM (BiLSTM) deep-learning architecture
- TensorFlow-based model training
- Custom dataset collected from YouTube and Twitter comments
- Text tokenization for preprocessing
- Evaluation using test accuracy, loss, and class-wise classification metrics
- Training and evaluation workflow implemented in a Jupyter Notebook

## Tech Stack

- **Language:** Python
- **Deep Learning:** TensorFlow
- **Data Processing:** NumPy, pandas
- **Evaluation:** scikit-learn
- **Visualization:** Matplotlib, Seaborn
- **Development Environment:** Jupyter Notebook

## Dataset

The model uses a custom dataset stored in `DATA_2.csv`, containing comments collected from YouTube and Twitter.

| Property | Details |
|---|---|
| Dataset file | `DATA_2.csv` |
| Data sources | YouTube and Twitter comments |
| Dataset type | Custom-collected text dataset |
| Approximate samples per sentiment class | 3,000+ |
| Classification labels | Positive, Negative, Neutral |
| Data partitions | Training, validation, and testing |

The dataset is organized around three sentiment categories. Text tokenization is used to prepare the comments for model training.

The exact data split ratios and additional preprocessing parameters are not specified here.

## Model Architecture

The project uses a **Bidirectional Long Short-Term Memory (BiLSTM)** network implemented with TensorFlow.

LSTM networks are designed to learn sequential patterns in data. A bidirectional configuration processes a sequence in both forward and backward directions, allowing the network to learn contextual information from both sides of the sequence.

In this project, the BiLSTM is used to learn patterns in tokenized comments for three-class sentiment classification.

### Workflow

1. **Load the dataset:** Read the comments and their sentiment labels from `DATA_2.csv`.
2. **Preprocess the text:** Tokenize the text to prepare it for model training.
3. **Prepare data partitions:** Use the training, validation, and test datasets for model development and evaluation.
4. **Train the model:** Train the TensorFlow-based BiLSTM on the labeled comments.
5. **Evaluate performance:** Assess the trained model using accuracy, loss, and class-wise classification metrics.
6. **Save the model:** Retain the trained model artifact.

The current workflow operates on dataset inputs through the notebook; a standalone interactive inference interface is not yet available.

## Results

The trained model achieved the following results:

| Metric | Training | Testing |
|---|---:|---:|
| Accuracy | 97.12% | 84.47% |
| Loss | 0.1345 | 0.4964 |

The model performs substantially better on the training data than on the test data. This gap suggests **possible overfitting**, indicating that generalization to unseen comments could be improved.

### Test Classification Report

| Sentiment | Precision | Recall | F1-score | Support |
|---|---:|---:|---:|---:|
| Positive | 0.85 | 0.84 | 0.85 | 675 |
| Negative | 0.82 | 0.82 | 0.82 | 674 |
| Neutral | 0.86 | 0.87 | 0.87 | 653 |
| **Macro average** | **0.84** | **0.84** | **0.84** | **2,002** |
| **Weighted average** | **0.84** | **0.84** | **0.84** | **2,002** |

The model achieves reasonably consistent performance across all three sentiment classes. Neutral sentiment has the highest F1-score, while negative sentiment has the lowest among the three classes.

The test results indicate that the model can learn useful sentiment patterns, although its performance on unseen data remains below its training performance.

## Visualizations

The repository includes plots related to the model's training and evaluation.

These visualizations can help examine model performance and understand the difference between training and test results.

## Running the Project

The project is implemented in a Jupyter Notebook and uses `DATA_2.csv` as its dataset input.

To work with the project:

1. Clone or download the repository.
2. Set up a Python environment with the dependencies used by the notebook.
3. Ensure that `DATA_2.csv` is available at the file location expected by the notebook.
4. Open the notebook in Jupyter Notebook or a compatible environment.
5. Run the notebook cells in sequence to execute the implemented workflow.

The repository's actual notebook filename and dependency versions should be used when configuring the environment. No specific execution command or saved-model filename is documented here because those details have not been confirmed.

## Limitations

- **Potential overfitting:** Training accuracy is 97.12%, compared with 84.47% test accuracy.
- **Dataset limitations:** The dataset's size, diversity, and representativeness may limit how well the model generalizes to other text sources.
- **Context and language nuances:** Sarcasm, slang, ambiguous wording, and context-dependent expressions can make sentiment classification difficult.
- **Domain variation:** Performance may vary across platforms, topics, and writing styles.
- **Limited inference interface:** The current implementation operates through a notebook and dataset workflow rather than a standalone interface for entering individual comments.

## Future Improvements

Potential improvements include:

- Investigating regularization and other methods to reduce overfitting.
- Expanding the dataset with more diverse topics, writing styles, and examples.
- Evaluating performance on additional unseen datasets.
- Improving text preprocessing and handling of slang, sarcasm, and ambiguous expressions.
- Building an inference interface that accepts individual text inputs.
- Exploring additional evaluation visualizations and model configurations.

## Learning Outcomes

This project provided practical experience with:

- Text classification using deep learning
- Bidirectional recurrent neural networks
- TensorFlow model training and evaluation
- Text preprocessing and tokenization
- Classification metrics and model generalization
- Working with a custom dataset of social-media comments

## Author

**Punyam Gupta**

GitHub: [@Punyam22](https://github.com/Punyam22)

---

This project was developed as a portfolio project to explore deep-learning-based sentiment analysis on social-media text.

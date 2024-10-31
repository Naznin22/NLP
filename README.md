# Sentiment Analysis with BERT and ktrain
This project demonstrates a sentiment analysis model using BERT for text classification. The model leverages TensorFlow and ktrain, a wrapper for TensorFlow Keras, which simplifies the model-building and training process.

## Overview
The project uses the IMDB movie reviews dataset to classify sentiments as either positive or negative. It employs the BERT language model, known for its state-of-the-art performance in NLP tasks. By integrating ktrain with TensorFlow, the model achieves efficient training, evaluation, and deployment.

## Requirements
To run this project, install the required Python packages:

* tensorflow==2.15.1
* tf_keras
* ktrain
* Additional Requirement: Set the TF_USE_LEGACY_KERAS environment variable to "1" to ensure compatibility with Keras 3, which may not yet be fully supported by ktrain.

## Dataset
The project uses the IMDB movie reviews dataset, which contains labeled data for positive and negative sentiment classification. The data is organized into train and test folders and is preprocessed with ktrain’s text module for BERT model compatibility.

## Project Structure
* Data Loading and Preprocessing: The IMDB dataset is downloaded and organized into positive and negative classes. Preprocessing steps include setting the maximum sequence length and tokenizing the text with BERT’s tokenizer.

* Model Building: Using the BERT architecture for text classification, the model is set up for binary sentiment classification with ktrain, which makes model building and fine-tuning efficient.

* Training the Model: The model is trained with a one-cycle learning rate policy, recommended for optimal performance. The batch size and epoch count are configured to balance training time and accuracy, making it relatively lightweight for quick testing.

## Notes
* Learning Rate: The model uses a learning rate of 2e-5, as recommended for training BERT models in this configuration.
Batch Size and Epochs: Training is performed with a batch size of 6 and a single epoch, making it suitable for faster training iterations and experimentation.
## Results and Evaluation
After training, the model can be evaluated on unseen data to assess its accuracy in predicting sentiment labels, providing insights into its effectiveness for sentiment analysis tasks.

## Acknowledgments
This project is built using TensorFlow and ktrain. The IMDB movie review dataset is provided by Stanford University.

# Music Genre Classification
## 1. Project Overview
This project focuses on creating a Music Genre Classifier using the GTZAN dataset, leveraging a pre-trained DistilHuBERT model for feature extraction, and utilizing the Hugging Face Hub for model fine-tuning and hosting. Gradio is employed to build a user interface that allows users to classify music genres based on audio input.
## 2. Dataset
GTZAN Dataset
The GTZAN dataset is accessed through the Hugging Face datasets library. The dataset is then divided into training and test sets, ensuring that 10% of the data is reserved for evaluation.
## 3. Data Preprocessing
Feature Extraction
A pre-trained DistilHuBERT model is used to extract features from the audio data. The audio files are converted to match the feature extractor's sampling rate, ensuring consistency across the dataset. The audio samples are truncated to a maximum duration of 30 seconds to standardize input length for the model.
Preprocessing Function
A preprocessing function is applied to the dataset to extract features and generate attention masks. This prepares the data for input into the model.
## 4. Model Fine-Tuning
Model Preparation
The DistilHuBERT model is configured for audio classification. The genres in the GTZAN dataset are mapped to numeric labels for training purposes.
Training Configuration
The model is trained using the Hugging Face Trainer API, which allows for easy configuration of training parameters such as batch size, learning rate, and the number of epochs. The model is evaluated at the end of each epoch, and the best-performing model is saved based on its accuracy.
Metrics
Accuracy is used as the primary evaluation metric during training and validation to assess the model's performance.
## 5. Deployment and Inference
Pushing Model to Hugging Face Hub
After the training process, the model is pushed to the Hugging Face Hub for hosting, making it easily accessible for future use.
Gradio User Interface
Gradio is utilized to create an interactive user interface, where users can upload audio files and receive predictions about the genre of the music.
## 6. Inference Pipeline
An inference pipeline is established to simplify the process of using the trained model for predictions. Users can input an audio file, and the model will output the predicted genre along with the associated confidence scores.
## 7. Conclusion
This project illustrates the implementation of a music genre classifier using advanced tools such as Hugging Face Transformers, Gradio, and the GTZAN dataset. By employing a pre-trained DistilHuBERT model and fine-tuning it for this specific task, the classifier can effectively recognize and predict various music genres with high accuracy.

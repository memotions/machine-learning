# Memotions Machine Learning
Memorize Your Emotions! ☺️ <br>

**Memotions** is a mental wellness app designed to support Indonesian users of all ages through personalized journaling, machine learning, and gamification features, such as streaks and achievements. The app utilizes machine learning models to perform Natural Language Processing (NLP) tasks. Our key models include:
- **Mood Classification**: Accurately identifying the user's mood based on their journal entries.
- **Personalized Suggestion**: Offering tailored recommendations to improve mental well-being.

## Dataset
For our mood classification model, the dataset consists of over 380,000 rows of labeled text in Bahasa Indonesia. The labels are divided into five classes: sad, happy, neutral, anger, and fear. This dataset was compiled from the following public sources: <br>

[English Dataset](https://www.kaggle.com/datasets/nelgiriyewithana/emotions) <br>
[Indonesian Dataset I](https://github.com/IndoNLP/indonlu/tree/master/dataset/emot_emotion-twitter) | [Indonesian Dataset II](https://github.com/meisaputri21/Indonesian-Twitter-Emotion-Dataset)

On the other hand, the dataset for fine-tuning the Gemini 1.0 Pro model consists of 50 rows of synthetic data generated using AI, with additional manual customizations to align with our specific tasks.

All the dataset can be found on the `datasets` folder.

## Machine Learning Model
### Mood Classification Model
This model processes user journal entries and classifies them into five categories: sad, happy, neutral, angry, and scared. Each entry is preprocessed into indexed and padded tensors before making predictions.
- Architectures : Bidirectional LSTM with Embedding Text Representation [EXAMPLE]
- Number of epochs : xxx
- Total parameters : xxx
- Learning rate : xxx

### Personalized Suggestion Model
This model is designed to provide one-paragraph suggestions based on users' entries. It has been developed with a focus on understanding and responding to user input, fine-tuned using Gemini 1.0 Pro, tuned and deployed via Vertex AI.
- Number of epochs : 3
- Learning rate multiplier : 0.1
- Adapter size : 16

## Results
### Mood Classification Model
The model achieved an accuracy of xx% and an F1 score of xx% on the test dataset. Below, we provide the learning graph and the confusion matrix for all classes.

### Personalized Suggestion Model
The model experienced fluctuating loss at each training step, ultimately ending with a value of 1.86. Below, we provide the corresponding graph.

![](https://github.com/user-attachments/assets/e371aa63-7fb3-40b8-a40f-cac865f91738)

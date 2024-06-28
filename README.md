# Chatbot Development Using NLP and Deployment with Flask and JavaScript

## Objective:
Design and implement a conversational AI chatbot capable of answering common candidate queries and guiding them through the job application process. The chatbot will leverage Natural Language Processing (NLP) to handle interactions effectively, providing a seamless and efficient experience for job applicants.

## Project Features:
This Chatbot can be integrated into both websites and mobile apps. These are conversational tools that act like a messaging app, where a candidates sends their question or issue and the bot provides an answer.

## Methodology Description: Chatbot Development for Job Application Guidance
* Python: Programming language used for development.
* PyTorch: Deep learning framework for building and training neural networks.
* NumPy: Library for numerical operations.
* NLTK (Natural Language Toolkit): Library for natural language processing tasks (used indirectly through nltk_utils).
* PyTorch: Deep learning framework for building and training neural networks.

## Step-by-Step Methodology:
### 1. Tokenization:
Function: tokenize(sentence)
Description: This function takes a sentence as input and splits it into an array of words/tokens. A token can be a word, punctuation character, or number.
Implementation: Uses nltk.word_tokenize to split the sentence.

### 2. Stemming:
Function: stem(word)
Description: This function finds the root form of a given word. For example, it reduces "organize", "organizes", and "organizing" to "organ".
Implementation: Uses the PorterStemmer from the NLTK library to stem words.

### 3. Bag of Words:
Function: bag_of_words(tokenized_sentence, words)
Description: This function converts a tokenized sentence into a bag-of-words (BoW) array. The BoW array has 1 for each known word that exists in the sentence and 0 otherwise.
Implementation:
* Stem each word in the tokenized sentence.
* Initialize a zero array with the same length as the known words list.
* Set the corresponding index to 1 if the stemmed word exists in the known words list.

### 4. Neural Network Model:
After performing NLTK operations on text data, neural network model is likely to benefit from improved generalization, enhanced semantic understanding, and more efficient training. These operations help in standardizing and preparing text inputs to be more suitable for learning patterns and making predictions based on the semantics of the text rather than superficial variations. This can lead to a more robust and effective chatbot or NLP application overall.

## Application:
Chatbot Interaction: When a user inputs a query, the chatbot tokenizes and stems the input sentence, converts it into a BoW vector, and uses this vector to determine the most appropriate response based on pre-trained machine learning models or predefined rules.
Candidate Guidance: The chatbot can effectively answer common candidate queries about the job application process by matching the input query to the most relevant responses in its knowledge base.

## Result and Performance
### Model Accuracy:
![image](https://github.com/Pacchu04/ChatBot/assets/92878457/5801b278-3469-4777-86fe-1041362792bb)

### Result:
![image](https://github.com/Pacchu04/ChatBot/assets/92878457/41017b7c-1eb6-49df-b103-b99bf795d783)

![image](https://github.com/Pacchu04/ChatBot/assets/92878457/7d812d5a-2bd4-46d8-b01e-2ce123ad2133)

## Initial Setup:

Clone repo and create a virtual environment
```
$ git clone https://github.com/python-engineer/chatbot-deployment.git
$ cd ChatBot
$ python -m venv venv
$ venv\Scripts\activate
```

Install dependencies
```
$ (venv) pip install Flask torch torchvision nltk
```
Install nltk package
```
$ (venv) python
>>> import nltk
>>> nltk.download('punkt')
```
Modify `intents.json` with different intents and responses for your Chatbot. It contains a conversation data between the bot and the candidate. Modify the files based on your company’s process.

After each time modification of `intents.json' file Run the below commond mandatory.

Run
```
$ (venv) python train.py
```
This will dump data.pth file. And then run

The following command to test the chatbot in console.
```
$ (venv) python chat.py
```
To run the Bot in application 
```
$ (venv) python app.py
```

# Semantic-search-models-for-chatbots
Testing semantic search models, in this case, sentence transformers (please refer to S-BERT: https://www.sbert.net/), for the task of user input comprehension and mapping to a rule-based chatbot's paths, here called 'options', which correspond to buttons displayed in the chatbot UI. 


# For best experience
Use Google CoLab with GPU Runtime enabled for the fastest processing time. 

# Models
For this analysis, I selected 4 sentence transformers designed for semantic search, trained on various datasets and with a varied number of parameters. 

# Metrics
We are comparing the models based on their **accuracy** in user text's comprehension and **average time to compute** a prediction.

# Dataset
Provided dataset is created at Imperial College London for the task of testing the model for user input mapping to chatbot buttons. 
It includes a set of user inputs in response to a chatbot utterance, a list of possible 'options' (buttons), and a label, which corresponds to user's intention in their text. 
The semantic search models take user input and compute semantic similarity between the text and docs, which in this case, consist of chatbot button options. 
The model is trying to map the user input to one of the buttons. If the semantic similarity score is below a threshold, it is considered **OOD** = Out of Domain (unrelated to options).

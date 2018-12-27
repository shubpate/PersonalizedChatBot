### Personality Based Chatbot

The objective of our project is to develop a chatbot model which can adapt a human personality for responding to any question. Chatbots like slack bot, fb messenger bot etc. are already there, but they respond in a very generic way, without remembering any context. We want to give chatbot a personality, so that it can act like a human while responding.

We have tried two different approaches using two different frameworks -

1. Keras
2. Pytorch

Our main idea was to train the model on a conversation dataset with
the context-response pairs as follows: 

**Context (X-label) :** Concatenation of all the dialogues before him/her.

**Response (Y-label):** The dialogue of that particular person.

In case of personal chats, suppose a person wants to train a model on his own personality, Then he would take his chats and context response pairs would be generated as:

**Context (X-label):** The response of the opposite person

**Response (Y-label):** My response.

This was a very basic idea with the idea that if we somehow train a model to respond to a question in a specific way, then ultimately it would learn too.

In terms of **Dataset** we have used dialogues from famous TV sitcom **FRIENDS** and taken Ross as our primary speaker. So context response pairs are generated corresponding to his dialogues. While forming pair we have tried two different approaches, in first one we concatenate all the dialogues between two Ross's dialogues and treat it as it said by some individual alone. Then we have pairs of conversation from X and Ross. In another approach, we just concatenate last 5 dialogues spoken by other people before Ross. More details can be found on report. 

#### **Files to follow :**

For Keras implementation which used Gensim and LSTM with attention, follow the jupyter notebook mentioned below, you might need to make few changes depending on your run environment  -

**FRIENDS_Chat_Keras.ipynb**

For Pytorch implementation, which used one hot vector encoding and is build on top of a Seq2Seq model, follow the file mentioned below  -

**FriendsChatBot_over_seq2seq_Pytorch.ipynb**

Incase you prefer to use the same FRIENDS dataset please use the file mentioned below  -

**friends-final.txt**

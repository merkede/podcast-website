---
title: Wrap notes automation
summary: |
  Led two junior data scientists on a Net Zero Strategy project, developed an automation tool providing cost savings of £200k per annum. Delivered key recommendations and insights to Director and senior leadership.
date: 2021-06-13
categories:
  - Azure Machine Learning
  - Hugging Face transformers
  - NLP

links:
  - icon: link
    icon_pack: fas
    name: docs
    url: https://github.com/merkede3/Wrap_Note_Automation/blob/main/docs/project_plan.md
  - icon: github
    icon_pack: fab
    name: source
    url: https://github.com/merkede3/Wrap_Note_Automation/
---

### TL;DR

Our recent proof of concept (POC) demonstrated the successful integration of AWS and Salesforce, which allowed us to apply a summarization algorithm to a webchat transcript. The resulting webchat summary was able to replace and eliminate the need for webchat wrap notes, resulting in a roll-out providing cost savings of £200k annually.

### Defining the Problem

Centrica is experiencing a surge in demand for its Net Zero division and strategy, resulting in a significant increase in expected customer contact. This presents a challenge for the company, as it anticipates a rise in operating expenses (OPEX) due to the additional web chat and contact centre interactions. In light of this, the business must determine how to manage the growing demand for Net Zero while keeping OPEX costs under control. To address the challenge of managing the growing demand for Net Zero while keeping OPEX costs in check, our proposed solution was to automate the web chat wrap notes.

**Business perspective**

This approach would significantly reduce the time agents spend on each web chat conversation, allowing them to handle more calls and ultimately lower OPEX costs. By leveraging automation, Centrica would be able to effectively manage the increase in customer contact demand while optimizing its resources and maximizing efficiency.

**Customers perspective**

Customers will be able to access a web chat agent more frequently, resulting in reduced wait times. 
The use of summarization technology has the potential to increase the quality of repeat calls, as the algorithm is more effective in extracting key points of the conversation than agent notes. 
This will lead to a more efficient and effective customer experience, with faster response times and improved accuracy of the information provided.

### Definitions

Wrap - Wrap is the timeframe after a call or webchat conversation, during which the agent summarizes or notes the purpose and any key details of the call for future reference.

Wrap Notes - Wrap Notes are an agent's summary or notes that are inputted into the system to record the purpose, solution, and key details of a call for future reference.

Webchat transcript - A Webchat transcript is a complete written record of a conversation that takes place between a customer and an agent through a webchat interface. The transcript is typically saved and timestamped within the Salesforce system for future reference and analysis.

### Hugging Face 

Hugging Face is a popular open-source library for natural language processing (NLP) that provides a suite of pre-trained models for various NLP tasks such as text classification, question answering, language translation, and summarization. Hugging Face Transformers is the core of the library, providing an easy-to-use and efficient interface for working with these pre-trained models. It is built on top of PyTorch and TensorFlow, and provides a unified API for working with a wide range of pre-trained transformer-based models such as BERT, GPT, XLNet, and T5. The library also provides a number of tools for fine-tuning these pre-trained models on custom datasets, and for adapting them to specific downstream NLP tasks.
    
{{< figure src="img/hugging.jpg" caption="Hugging Face Endpoints on Azure" >}}

### Text Summarisation

NLP summarisation is a challenging task that requires a deep understanding of language, context, and domain-specific vocabulary. One of the primary considerations is the ability to understand the context of the text and accurately identify the most salient information. Another is the need to consider the nuances and subtleties of the language. This includes accounting for things like sarcasm, irony, and metaphor, which can significantly impact the meaning of the text. Moreover, summarisation should take into account domain-specific vocabulary or jargon, and this often required the curation of a custom dictionary.

**There are two main types of summarization: extractive and abstractive**

- Extractive summarisation 

Involves selecting a subset of sentences or phrases from the original text and using them to create a summary. This approach is relatively simple and can be very effective for summarising news articles or scientific papers, where the main ideas are often conveyed in a few key sentences. 

However, extractive summarisation can be less effective for longer or more complex texts, where the main ideas may be spread out across multiple sentences.
  
{{< figure src="img/summary.jpg" caption="The difference between abstractive and extractive summarisation" >}}

- Abstractive summarisation

Involves generating a summary that is not simply a copy of a subset of the original text, but rather a new text that conveys the main ideas and concepts of the original text in a concise and coherent manner. This approach can be more effective for summarising longer and more complex texts, as it allows the summariser to capture the main ideas of the text even when they are not expressed in a single sentence or paragraph. 

However, abstractive summarisation can be more challenging than extractive summarisation, as it requires the summariser to have a deeper understanding of the text and to be able to generate new text that is both accurate and coherent.

### T5 transformer-model

The T5 (Text-to-Text Transfer Transformer) model is a powerful transformer-based neural network architecture for a wide range of natural language processing (NLP) tasks. It was introduced by researchers at Google in 2019 and has been fine-tuned on large amounts of text data, making it one of the most effective pre-trained language models available.

The model is called "Text-to-Text" because it is designed to handle a wide range of NLP tasks by transforming one piece of text into another, instead of treating each task as a separate problem. This is achieved by training the model to map a source input to a target output through a process called "task-specific conditioning." - allowing the same model to be used for a wide range of tasks, including summarisation.

T5 is a transformer-based model, which means it is built on the architecture of the transformer model introduced in the 2017 paper "Attention is All You Need."

{{< figure src="img/new_text_to_text.jpg" caption="A T5 transformer-based model" >}}

### Pre-trained model

My chosen model, from Hugging face, for the text-summarisaton task was a summarisation model based on the T5 architecture. T5 is a transformer-based model that was pre-trained on a large corpus of text data using a combination of unsupervised and supervised learning. The model was trained to perform a variety of NLP tasks, including language translation, question answering, and summarization.

The model was fine-tuned on a specific dataset of meeting summaries, which enables it to generate high-quality summaries of meeting transcripts. At a high-level, the summarization model works by first encoding the input text using the T5 transformer. The encoded representation of the input is then passed through a series of decoder layers, which generate the output summary one token at a time. The decoder layers use a combination of attention mechanisms and recurrent neural networks (RNNs) to generate the summary in a way that is both accurate and coherent.

### POC

- Data Cleaning

I first preprocessed the chat transcripts by removing irrelevant information such as greetings, goodbyes, and other non-relevant utterances. This was important to not only reduce the length of the text but also because not all webchat conversations are transferred to an agent with many being handled by the automated bot.

The size of the data used for the POC was wuite large - covering all conversations in 2022.

- Transfer Learning

I fine-tuned the pre-trained transformer model on a large dataset of web chat transcripts. I used a technique called transfer learning, which involves training the model on a large dataset and then fine-tuning it on a smaller dataset specific to the task at hand.

During the fine-tuning process, I implemented a number of techniques inclding attention masking, learning rate scheduling, and gradient clipping to optimize the performance of the model. I also performed hyperparameter tuning to ensure that the model was fine-tuned with the best possible configuration.

Providing customers with a spare replacement hub adaptor for every purchase costs less than the combined cost of customers calling to order a replacement and filing a complaint for a broken adaptor. This is because the cost of these customer service interactions is higher than the unit cost of the product.

- Results

The resulting summarisation system was highly effective in identifying the most important information in the transcripts. The model was able to produce summaries that were concise and informative, highlighting the most salient information from the conversation betweeen agent and customer - including phone numbers, reference booking numbers and reschedules dates.

To evaluate the quality of the summaries, I used standard evaluation metrics such as ROUGE and F1 score. This proved my project successfull and demonstrated the effectiveness of using pre-trained transformer models for summarising web chat transcripts in a business setting.

{{< figure src="img/summarisation.jpg" caption="The summarisation process" >}}

### Delivery

Following the success of our proof of concept, the AWS platform engineers and Salesforce architects collaborated to integrate our model into the HIVE web chat system. The integration was specifically focused on 'sales conversations'.

In light of our findings, the business decided to conduct a trial by discontinuing the recording of wrap notes for web chat conversations. My analysis revealed that less than 30% of all HIVE calls were repeated, and there was little evidence that wrap notes were necessary.

This resulted in significant time and cost savings for the business, prompting a full transition to the AWS Connect platform. Once the transition is complete, my model will be reinstated and further tested.

{{< figure src="img/AWS_Salesforce.png" caption="The trial helped justify the business move to connect Salesforce to AWS Connect" >}}

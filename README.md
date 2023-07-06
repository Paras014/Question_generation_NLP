# Question_generation_NLP
## Introduction 
This project aims to generatte questions from given text .
## Workflow
![TExt file](https://github.com/Paras014/Question_generation_NLP/assets/98278584/d32bc18e-7c4d-4f13-8881-e6a6b8b02ecc)
## Description 
So the goal of this process is to automate making question , it could be used for making question for comprehension passages etc . 
## Step 1 
As per the workflow we first take the text data and summmarize it using BERT extractive sumarizer.
# BERT extractive summarizer vs BERT abstractive summarizer 
In BERT extractive summarizer every sentnce from the text is givven a score as per its importance and then the sentences with the highest scores are just extracted from the original text , while in bert abstractive summarizer it is summarization how a human would do it , read the text first and then write them in your own words , it takes all the text and from the context vector it generates paraphrased sentences unlike the extractive summarizer which just extracts the sentences from the given data . So basically the the ouput from the BERT extractive summarizer is a subset of the original text file.


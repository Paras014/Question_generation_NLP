# Question_generation_NLP
## Introduction 
This project aims to generatte questions from given text .
## Workflow
![TExt file (3)](https://github.com/Paras014/Question_generation_NLP/assets/98278584/7c5f07fd-aaa7-4867-bcda-d654d92f6756)
## Description 
So the goal of this process is to automate making question , it could be used for making question for comprehension passages etc . 
# Step 1 (Summarization)
As per the workflow we first take the text data and summmarize it using BERT extractive sumarizer.You can use any other transformer like GPT , T5 etc .
## BERT extractive summarizer vs BERT abstractive summarizer 
In BERT extractive summarizer every sentnce from the text is givven a score as per its importance and then the sentences with the highest scores are just extracted from the original text , while in bert abstractive summarizer it is summarization how a human would do it , read the text first and then write them in your own words , it takes all the text and from the context vector it generates paraphrased sentences unlike the extractive summarizer which just extracts the sentences from the given data . So basically the the ouput from the BERT extractive summarizer is a subset of the original text file.
# Step 2 (Keyword extraction)
In this step the important keywords are extracted which act as the answer to the questions, the keyword extraction can be done in various ways , there are many libraries that can be used for keyword extraction like spaCY , Rake nltk , Gensim , YAKE , you can use any of these . All the keywords are stored in the list. 
# Step 3 (Keyword Sentence dictionary)
The sentences are found and extracted in which the extracted pairs and stores in the dictionary with keys as the extracted word and the values are the sentences in which the extracted words are present , this is dony by simply using for loop. 
# Step 4  (Feeding data to tranformer )
A pretrained T5 transformer is used here which take in the text which is nothing but the answers and the sentnce concatenated , so th keys of the dictionary are added to the values which is then fed into the model as input . The model then generates question form the setences given .  
# Results 
ExampleInput text  - 
In p-block elements the last electron enters the outermost p orbital. As we know that the number of p orbitals is three and, therefore, the maximum
number of electrons that can be accommodated in a set of p orbitals is six. Consequently there are six groups of p–block elements in the periodic
table numbering from 13 to 18. Boron, carbon, nitrogen, oxygen, fluorine and helium head the groups. Their valence shell electronic configuration is
ns 2 np 1-6(except for He). The inner core of the electronic configuration may, however, differ. The difference in inner core of elements greatly
influences their physical properties (such as atomic and ionic radii, ionisation enthalpy, etc.) as well as chemical properties. Consequently, a lot
of variation in properties of elements in a group of p-block is observed. The maximum oxidation state shown by a p-block element is equal to the total
number of valence electrons (i.e., the sum of the sand p-electrons). Clearly, the number of possible oxidation states increases towards the right of
the periodic table. In addition to this so called group oxidation state, p-block elements may show other oxidation states which normally, but not
necessarily, differ from the total number of valence electrons by unit of two. The important oxidation states exhibited by p-block elements are shown
in Table 11.1. In boron, carbon and nitrogen families the group oxidation state is the most stable state for the lighter elements in the group.
However, the oxidation state two unit less than the group oxidation state becomes progressively more stable for the heavier elements in each group.
The occurrence of oxidation states two unit less than the group oxidation states are sometime attributed to the ‘inert pair effect’. <br>
<br>
Example Output - <br>
Where does the last electron enter the outermost p orbital?<br>
P-block elements
<br>
<br>

What enters the outermost p orbital?<br>
The last electron
<br>
<br>

Along with carbon, nitrogen, oxygen, fluorine and helium, what is the last group in p-block elements?<br>
Boron
<br>
<br>
Along with Boron, nitrogen, oxygen, fluorine, and helium, what element heads the group of p-block elements?<br>
Carbon
<br>
<br>

Along with boron, carbon, oxygen, fluorine and helium, what element heads the group?<br>
Nitrogen
<br>
<br>

Along with Boron, carbon, nitrogen, fluorine and helium, what element heads the group?<br>
Oxygen
<br>
<br>

Along with boron, carbon, nitrogen, oxygen and helium, what is the last group in p-block elements?<br>
Fluorine
<br>
<br>
Boron, carbon, nitrogen, oxygen, fluorine, and what other element head the groups?<br>
Helium
<br>
<br>
Boron, carbon, nitrogen, oxygen, fluorine and helium head what?<br>
The groups
<br>
<br>


What is the ns 2 of p-block elements?<br>
Their valence  shell electronic configuration
<br>
<br>

What is the only electronic configuration of p-block elements?<br>
He
<br>
<br>


What increases towards the right of the periodic table?<br>
The number
<br>
<br>


The number of what increases towards the right of the periodic table?<br>
Possible oxidation states
<br>
<br>

The number of possible oxidation states increases towards what part of the periodic table?<br>
The right
<br>
<br>


The number of possible oxidation states increases towards the right of what?<br>
The periodic table
<br>
<br>

The number of possible oxidation states increases towards the right of the periodic table.<br>
Addition
<br>
<br>

What may show other oxidation states which normally, but not necessarily, differ from the total number of electrons by unit of two?<br>
This so called group oxidation state, p-block elements 
<br>
<br>

Besides group oxidation states, what else may p-block elements show?<br>
Other oxidation states
<br> 
<br>

Boron, carbon, nitrogen, oxygen, fluorine and helium head the groups of what? <br>
Which
<br>
<br>

What does the number of oxidation states by unit of two differ from?<br> 
The total number
<br>
<br>

Boron, carbon, nitrogen, oxygen, fluorine and helium head the groups with what electronic configuration?<br>
Valence electrons
<br>
<br>

How do p-block elements differ from the total number of oxidence electrons? <br>
Unit
<br>
<br>

What are shown in Table 11.1? <br>
The important oxidation states
<br>
<br>

Where does the last electron enter the outermost p orbital?<br>
P-block elements
<br>
<br>
Where are the important oxidation states exhibited by p-block elements shown?<br>
Table
<br>
<br>

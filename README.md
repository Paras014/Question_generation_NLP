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
Input text  - 
Sachin Tendulkar, in full Sachin Ramesh Tendulkar, (born April 24, 1973, Bombay [Mumbai], India), Indian professional cricket
player, considered by many to be one of the greatest batsmen of all time. In 2012 he became the first cricketer to score 100
centuries (100 runs in a single innings) in international play.  Tendulkar was given his first bat when he was 11 years of
age. As a 14-year-old, he used it to score 329 out of a world-record stand of 664 in a school match. A year later he scored a
century on his first-class debut for Bombay (Mumbai), and at age 16 years 205 days he became India’s youngest Test
(international) cricketer, making his debut against Pakistan in Karachi in November 1989. When he was 18 he scored two
centuries in Australia (148 in Sydney and 114 in Perth), and in 1994 he scored 179 against the West Indies. In August 1996,
at age 23, Tendulkar was made captain of his country’s team. Although India was defeated in the semifinals of the 1996 World
Cup, Tendulkar emerged as the tournament’s top run scorer, with 523 runs. In 1998 he was chosen for the Rajiv Gandhi Khel
Ratna Award, the highest award given to an Indian athlete, for his outstanding performance in the 1997–98 season. India was
defeated by Australia in the 1999 World Cup, failing to advance past the round of six, and was soundly defeated by both
Australia and South Africa in series later that year. In the 2003 World Cup, however, Tendulkar helped his team advance as
far as the finals. Though India was again defeated by Australia, Tendulkar, who averaged 60.2, was named the man of the
tournament Tendulkar made history in December 2005 when he scored his record-breaking 35th century in Test play against Sri
Lanka. The feat was accomplished in a total of 125 Tests and allowed Tendulkar to surpass the prolific Indian run scorer
Sunil Gavaskar. In June 2007 Tendulkar reached another major milestone when he became the first player to record 15,000 runs
in one-day international (ODI) play, and in November 2011 he became the first batsman to score 15,000 runs in Test play. One
month later he scored a historic “double century” in a contest against South Africa, becoming the first man in history to
record 200 runs in a single innings of ODI play. He was named the 2010 International Cricket Council (ICC) Cricketer of the
Year. In an ODI match against Bangladesh in March 2012, Tendulkar scored his record-setting 100th international century—which
included both Test (51 centuries) and ODI (49 centuries) play. He retired from ODI cricket later that year, and in 2013 he
ended a six-year stint with the Indian Premier League (as a member of the Mumbai Indians) and retired from Test cricket,
ending his playing days with records for the most career international runs (34,357) and Test runs (15,921). Throughout his
long career Tendulkar was consistently ranked among the game’s best batsmen. He was often likened to Australia’s Don Bradman
in his single-minded dedication to scoring runs and the certainty of his strokeplay off both front and back foot.  In 2012
Tendulkar became a member of the Rajya Sabha, the upper chamber of the Indian parliament—the first active athlete to join
that body; he was nominated to the post, and his term ended in 2018. In 2014 he became the first sportsman to receive India’s
highest civilian honour, the Bharat Ratna. Tendulkar was inducted into the International Cricket Council Hall of Fame in
2019. <br>
<br>
Final Output - <br>
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

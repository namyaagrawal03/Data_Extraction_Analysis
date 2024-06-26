# Data_Extraction_Analysis

Data Extraction and NLP

**OBJECTIVE**
The objective of this assignment is to extract textual data articles from the given URL and perform text analysis to compute variables that are explained below. 

**Data Extraction**
Input.xlsx
For each of the articles, given in the input.xlsx file, extracted the article text and saved the extracted article in a text file with URL_ID as its file name.
While extracting text, made sure that the program extracts only the article title and the article text. It should not extract the website header, footer, or anything other than the article text. 

**Data Analysis**
For each of the extracted texts from the article, performed textual analysis and computed some variables.

  **Sentimental Analysis**
      Sentimental analysis is the process of determining whether a piece of writing is positive, negative, or neutral. The below Algorithm is designed for use in Financial Texts. It consists of steps:
      **Cleaning using Stop Words Lists**
      The Stop Words Lists (found in the folder StopWords) are used to clean the text so that Sentiment Analysis can be performed by excluding the words found in Stop Words List. 
      **Creating a dictionary of Positive and Negative words**
      The Master Dictionary (found in the folder MasterDictionary) is used for creating a dictionary of Positive and Negative words. Added only those words in the dictionary if they are not found in the Stop 
      Words Lists. 
      
  
  **Variables:**
  
  **1. Positive Score:** This score is calculated by assigning the value of +1 for each word if found in the Positive Dictionary and then adding up all the values.
      
  **2. Negative Score:** This score is calculated by assigning the value of -1 for each word if found in the Negative Dictionary and then adding up all the values. We multiply the score with -1 so that the score                            is a positive number.
      
  **3. Polarity Score:** This is the score that determines if a given text is positive or negative in nature. It is calculated by using the formula: 
                              Polarity Score = (Positive Score – Negative Score)/ ((Positive Score + Negative Score) + 0.000001)
                              Range is from -1 to +1

  **4. Subjectivity Score:** This is the score that determines if a given text is objective or subjective. It is calculated by using the formula: 
                              Subjectivity Score = (Positive Score + Negative Score)/ ((Total Words after cleaning) + 0.000001)
                              Range is from 0 to +1
  
  
  **5. Average Sentence Length** = the number of words / the number of sentences
  
  **6. Percentage of Complex words** = the number of complex words / the number of words 
  
  **7. Fog Index** = 0.4 * (Average Sentence Length + Percentage of Complex words)

  **8. Average Number of Words Per Sentence** = the total number of words / the total number of sentences
  
  **9. Complex words** : They are words in the text that contain more than two syllables.

  **10. Word Count** : We count the total cleaned words present in the text by :
                    -removing the stop words (using stopwords class of nltk package).
                    -removing any punctuations like ? ! , . from the word before counting.

  **11. Syllable count per word:** We count the number of Syllables in each word of the text by counting the vowels present in each word. We also handle some exceptions like words ending with "es","ed" by not                               counting them as a syllable.
  
  **12. Personal Pronouns** : To calculate Personal Pronouns mentioned in the text, we use regex to find the counts of the words - “I,” “we,” “my,” “ours,” and “us”.
  
  **13. Average word lenght** : Sum of the total number of characters in each word/Total number of words


**OUTPUT**
 The output is stored in a file caleed “Output Data Structure.xlsx”

# Data-Bias-Project-2
## An Analysis of Hidden Religious Biases in Google's API Comment Toxicity API. 


## Motivations
The intial goal of my analysis was to examine the construction of the Perspective API released by Google Jigsaw for potential biases. This examination was done through querying the existing natural language processing model. For reference, Perspective defines toxicity as a rude, disrespectful, or unreasonable comment that is likely to make you leace a discussion. I started by forumulating several queries in order to gain an understanding of how the API was scoring each comment. Right away I noticed several potential areas within that API that could hold hidden biases or could be prone to miscalculations. The program did not recognize the use of the word "mangina" and was unable to provide a toxicity score despite it being referenced in the text. This error could point to a flaw in the language processing model in that merged words or slang words are not coded in to the system. Another potential bias I found was in the use of the words "dick" or "vagina", specifically in the sentence "I love dick more than anything". Despite the only word with a high toxicity score being 'dick' (0.59), the sentence was rated at a 0.83 toxicity score. It is true that 'dick' could be considered sexually explicit but the wording of the sentence could also make the phrase considered an expression of love. Perhaps the API is encorporating the socio-cultural impact of homophobia when it is ranking toxicity scores related to anatomical organs. Could the ranking system be influenced by the primary demographic of the users that the API is drawing its source database from? My third examination is the one that I choose to form my hypothesis around. While analysing the toxicity scores of different words I noticed that the names of different religions garnered different rankings. Christian was the lowest (0.027), then Muslim was ranked .137 points higher at (0.162), and Jewish was ranked 0.109 points higher then Muslim and 0.244 points higher then Christian (0.271). I continued to explore related terms to each of the three main religions and found that the name of the religious book associated with each religion also received different scores: Bible (0.022), Quran (0.028), and Torah (0.029). A future area of research would be examining the underlying narratives that have created the perceptual differences between each religion. If a person with a background in relgious studies continued this research I am sure that they would be able to identify the origin of the different calculations and what that says about Western society. The results of my anlysis are provided on Get Hub under the name "Data Bias Project 2" and Jupyter Notebook under the name "Data Bias (v1)". 

## Build Status
In the future I would recommend using a bigger and more expansive data set to test the Perspective API and its correlation to religious biases. It would also be more accurate if an expert in religious studies or in data analytics examined the same code. 

## Code Style and Framework 
All files are compatible with Python and were created in version 2.5 of Jupyter Notebook using Python 3 on a MacBook Air.

## Installation

For installation the User would need a computer with version 3.0 of Python and 2.5 of Jupyter Notebook. In order to gain access to the Perspective API you need to first create a google cloud account at console.cloud.google.com then follow the instructions on the Perspective webpage here https://support.perspectiveapi.com/s/docs-get-started. 

## API Reference

## License 
MIT: public domain license. 

## Credit
Dr. Engler, Perspective API



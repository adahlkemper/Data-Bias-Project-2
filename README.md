# Data-Bias-Project-2
## An Analysis of Hidden Religious Biases in Google's API Comment Toxicity API. 


## Motivations
The intial goal of my analysis was to examine the construction of the Perspective API released by Google Jigsaw for potential biases. This examination was done through querying the existing natural language processing model. For reference, Perspective defines toxicity as a rude, disrespectful, or unreasonable comment that is likely to make you leace a discussion. I started by forumulating several queries in order to gain an understanding of how the API was scoring each comment. Right away I noticed several potential areas within that API that could hold hidden biases or could be prone to miscalculations. The program did not recognize the use of the word "mangina" and was unable to provide a toxicity score despite it being referenced in the text. This error could point to a flaw in the language processing model in that merged words or slang words are not coded in to the system. Another potential bias I found was in the use of the words "dick" or "vagina", specifically in the sentence "I love dick more than anything". Despite the only word with a high toxicity score being 'dick' (0.59), the sentence was rated at a 0.83 toxicity score. It is true that 'dick' could be considered sexually explicit but the wording of the sentence could also make the phrase considered an expression of love. Perhaps the API is encorporating the socio-cultural impact of homophobia when it is ranking toxicity scores related to anatomical organs. Could the ranking system be influenced by the primary demographic of the users that the API is drawing its source database from? My third examination is the one that I choose to form my hypothesis around. While analysing the toxicity scores of different words I noticed that the names of different religions garnered different rankings. Christian was the lowest (0.027), then Muslim was ranked .137 points higher at (0.162), and Jewish was ranked 0.109 points higher then Muslim and 0.244 points higher then Christian (0.271). 

  I continued to explore related terms to each of the three main religions and found that the name of the religious book associated with each religion also received different scores: Bible (0.022), Quran (0.028), and Torah (0.029). Moreover, I found that the context in which terms were used was differentiated between the three groups - especially when it came to the labeling the people who followed each belief system. Christians were rarely mentioned in upfront, derogatory ways. Often if a comment had been flagged for toxicity with the mention of Christians it became apparent that the writer was a Christian and within the text was defending their faith while de-moralizing the other participant(s) in the conversation. There were few, if any, texts that explicity stated 'kill all christians'. The same can not be said for the references to the word 'jew', 'jewish', 'muslim', or 'islamic'. While a large degree of contextual comments for the afforementioned words were discussion oriented - usually conversations/analysis of religion or geo-political histories. The words 'jew', 'jewish', 'muslim', or 'islamic' were used to a higher degree then the word 'christian' or 'christains' in sentences associated with hate speech. There were several comments that explicity wished ill or death to the groups the words referred to, or used the word itself as an insult. White, western stereotypes were also ingrained in the sentences. For example, 'jew' often returned comments that disccussed race, genetics, and heriditary characteristics while 'muslim' or 'islamic' returned comments associated with fanatacism, war/military, and general anti-islamic sentiments. Right now, the toxcicity scores are a reflection of deep-rooted cultural biases and if they go unaddressed it will create inaccurate assumptions in the future. 
  
  A future area of research would be examining the underlying narratives that have created the perceptual differences between each religion. If a person with a background in relgious studies continued this research I am sure that they would be able to identify the origin of the different calculations and what that says about Western society. The results of my anlysis are provided on Get Hub under the name "Data Bias Project 2" and Jupyter Notebook under the name "Data Bias (v1)". 

## Build Status
In the future I would recommend using a bigger and more expansive data set to test the Perspective API and its correlation to religious biases. In addition, a more rigerous test that contained more variations of each word would provide more depth to the findings and ensure that no terms were left out. The program would also be more accurate if an expert in religious studies or in data analytics examined the same code. 

## Code Style and Framework 
All files are compatible with Python and were created in version 2.5 of Jupyter Notebook using Python 3 on a MacBook Air. In order to create the code, the program also used Perspective API, Pandas, Time, and Conda. 

Examples of Code

Calling Forward Specific Comments:
![Screen Shot 2022-10-17 at 11 01 13 PM](https://user-images.githubusercontent.com/113537319/196333761-fefd988f-4e9c-49f3-a83e-f2e1cdecf234.png)

Multi-Variable Analysis: 

![Screen Shot 2022-10-17 at 11 01 35 PM](https://user-images.githubusercontent.com/113537319/196334599-c3ad96fe-4f48-4f02-8b85-9032bb12b97b.png)

Examining the Toxicity Score of a Word:
![Screen Shot 2022-10-17 at 11 01 54 PM](https://user-images.githubusercontent.com/113537319/196333798-3d40cdc4-bff2-4ee0-bed6-0d275314c7b4.png)



## Installation

For installation the User would need a computer with version 3.0 of Python and 2.5 of Jupyter Notebook. In order to gain access to the Perspective API you need to first create a google cloud account at console.cloud.google.com then follow the instructions on the Perspective webpage here https://support.perspectiveapi.com/s/docs-get-started. 

The link for the Wikipedia Dataset:
http://localhost:8888/edit/labeled_and_scored_comments.csv

The Link for The Original Jupyter Notebook Code:
http://localhost:8888/notebooks/Data%20Bias%20(v1).ipynb

## API Reference
AIzaSyClhOaJW7IZtxkzsAVEUtXMaqR0zlD749U

## License 
MIT: public domain license. 

## Credit
Dr. Engler, Perspective API



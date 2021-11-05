# OAF-Industry-Classification
This github repository serves as a report for the Open Avenues Foundation Industry Classification micro internship. It shows our team's work on a NLP project, namely: classifying 20,000 companies into their industries (out of 13) based on their descriptions. 

Here you can find the documentation on the different stages of the project such as the data cleaning stage, applying different vectorization techniques, and then implementing versions of basic topic and unsupervised sentence classification. 

# DATA PREPROCESSING
A preprocessing function was created to clean the company description data first. Several cleaning techniques were used such as: 
- Regex(clean up email address, phone numbers, emojis, etc)
- removing stop words
- lemmatizing(using spacey)
- stemmer

# VECTORIZING
After data was cleaned, sentences were fed into TD-IDF to vectorize word to numeric data. By using TF-IDF, a statistical measure of each word's uniqueness relative to the rest of the data was found. Essentially, this step allowed the filtering of the most important words.

# USING LDA MODEL
One of the methods of classification we used was applying Laten Dirichtlet Allocation. By feeding our vectorized descriptions, LDA computed a probability of which industry each of  the descriptions had. More specifically:
![readme1](https://user-images.githubusercontent.com/19886626/140465462-40943131-717d-428e-9196-cbb1485cd323.png)

We found that the model gave decent satisfactory results, given the fact that many companies fell into more than one industry. 

Below is a word cloud depicting the the rankings of the industries predicted by our model:

![ldawordcloud](https://user-images.githubusercontent.com/19886626/140468289-ec94fecc-b9fc-4b11-a04a-ad5db92d8f4b.png)




# USING WORD EMBEDDINGS
Another classification model we implemented was through word embeddings. This model was more promising than LDA, since it involved taking into account the relevance of each word relative to each other and lumps similiar words together. We applied the model to both the company descriptions, the industry descriptions, and then compared each vectorized score from the company to match the closest one from the industry data set. Below is an example that shows the process of this technique

![shoes order](https://user-images.githubusercontent.com/19886626/140466050-4dc7a448-a322-480c-818e-4d4445affc19.png)

Word embedding model gave us results that were a hit or miss, with quite a few hits more than misses.
Overall I was satisfied with out results for this model.
Classified industries ranked:
![wordembeddingwordcloud](https://user-images.githubusercontent.com/19886626/140468677-969651c5-3cfb-4592-a10b-9b94384b3c90.png)

# CONCLUSION
This one month long project was incredibly rewarding in terms of how much I learnt topics such as
- Working with a large data science project
- Data cleaning
- Experimentation with different models such as K-means, LDA, word embedding and comparing their strengths and weaknesses.

Given that our data set was only 20,000 and more data pre processing could have been done, our model results were not expected to be superbly accurate. However, undertaking the project under such constraints allowed us to think critically on program optimization, and forced us to learn challenging concepts through implementation.  I am look forward to  pursuing more data science projects in the future. 

Unigram/Bigram/Trigram Operations:

This is an important section in Natural Language Processing (NLP) which mainly deals with human languages.

Lets us say if we want to analysis a sentence such as "This morning the weather was not as warm as yesterday morning". 

The unigram operation gives us: ('This', 'morning', 'the', 'weather', 'was', 'not', 'as', 'warm', ...). 

However, most of the times signle words cannot convey the appropriate meaning.

To improve the accuarcy of our model, we can implement the bigram and trigram operations:

Bigram result: ('This morning', 'morning the', 'the weather', 'weather was', 'was not', 'not as', 'as warm' ...).

Trigram result: ('This morninng the', 'morning the weather', 'the weather was', 'weather was not', 'was not as', 'not as warm', 'as warm as', 'warm as yesterday', ...).

After saving our obtained results from Unigram, Bigram, and Trigram operations, we can calculate the score of Term Frequency–Inverse Document Frequency (TF-IDF) for each of these models. I will create a new repository for the TF-IDF implementation. 

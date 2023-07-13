## Unigram, Bigram, and Trigram Features

Lets us say if we want to analysis a sentence such as "This morning the weather was not as warm as yesterday morning". 
The unigram operation gives us: ('This', 'morning', 'the', 'weather', 'was', 'not', 'as', 'warm', ...). 
However, most of the times single words cannot convey the appropriate meaning.
\
\
In order to **improve the accuarcy** of our model, we can implement the bigram and trigram operations:

Bigram result: ('This morning', 'morning the', 'the weather', 'weather was', 'was not', 'not as', 'as warm' ...).

Trigram result: ('This morninng the', 'morning the weather', 'the weather was', 'weather was not', 'was not as', 'not as warm', 'as warm as', 'warm as yesterday', ...).

After saving our obtained results from Unigram, Bigram, and Trigram operations, we can calculate the score of Term Frequency–Inverse Document Frequency (TF-IDF) for each of these models.

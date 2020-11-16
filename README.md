This is an important section in Natural Language Processing (NLP) which mainly deals with human languages.

Lets us say if we want to analysis a sentence such as "This morning the weather was not as warm as yesterday morning". 

The unigram operation give us: ('This', 'morning', 'the', 'weather', 'was', 'not', 'as', 'warm', ...). 
However, most of the times signle words cannot convey the appropriate meaening.

To improve the accuarcy of our model, we can implement the bigram and trigram operations:

Bigram result: ('This morning', 'morning the', 'the weather', 'weather was', 'was not', 'not as', 'as warm' ...).

Trigram result: ('This morninng the', 'morning the weather', 'the weather was', 'weather was not', 'was not as', 'not as warm', 'as warm as', 'warm as yesterday', ...).

# COMP 440: Representing and Retrieving Knowledge

Claude writes your answers here as you say them. A sentence or two is enough for each. Your
Part 0 predictions stay as you first wrote them; Part 5 asks what you would change.

**Name:** Oscar Reza Bautista
**Date:** 2026-10-20

## Part 0: Predictions

### Questions that name a character, place or thing: which method will do better, and why?

I expect TF-IDF to do better, since specific words will be highly weighted and things such as the characters or places of a movie will be very descriptive of what which movie we are talking about.

### Vague descriptions: which method will do better, and why?

I expect the embedding search to perform best, since word frequency might not play a big role given that a vague description does not give that much detail.

## Part 1: Build the TF-IDF model

### The settings you chose, and why

- `REMOVE_STOP_WORDS = True`: since I this will make TF-IDF vectors less sparse, hopefully making every entry more meaningful.
- `MIN_MOVIES = 1`: so that those summaries with uncommon words become more special.
- `REPEATS_COUNT_LESS = False`: because I think that greater difference between word frequencies will make vectors more representative of what they belong to.

## Part 2: Top terms

### Your movies: what do the top terms get right and wrong about what makes each one distinctive?

For Mulholland Drive, I think the word weights captures well the main characters in the film as well as some keywords to discuss the topic such as "ominous", "enigmatic", or "identity". However, it gives high importance to generic attributes such as "brunette" and "blonde", which I don't think are descriptive enough. For The Butterfly Effect, I think the first four most-ranked words are very representative of the film, but it is strange that words such as "memories" or "consequences" are ranked 9 and 10, respectively, appearing after "finds" which I'd say it does not say much.

## Part 3: Your own searches

### Your questions, as you typed them

A weapons manufacturer gets captured by a group of criminals and is forced to produce weapons for them. Noticing the harm that his inventions produce, he builds an armor that helps him escape and then goes on to become a superhero.
A confusing film of a guy who follows his death to another dimension.
McLovin and two other high schoolers try to fit in by providing alcohol for a party. Their journey is filled with funny moments and social commentary.

### Did the movies you meant come up? What did TF-IDF get right and wrong?

Only Iron Man came up for the first question, but it was numbered 10. The algorithm picked on key words for the descriptive questions, but really struggled with the vague one.

## Part 4: The question bank

### Which kind of question did TF-IDF handle best, and which worst? By how much?

It handled detail questions the best, identifying correctly 19 as first predictions. It really struggled with reworded and vague questions, with no correct predictions, not even within the top 10.

### The misses you looked at: what do they have in common?

Since synonyms are not the same words, it misses those semantic similarities completely, being unable to recognize questions that are saying pretty much the same as the overview, but with different words.

## Part 5: Embeddings

### What is a sentence embedding, in your own words?

A sentence embedding is a numeric representation of an input sentence; it is a vector of which the entries represent some feature or group of features of the sentence described. These features might not be explainable/understandable, since they are chosen algorithmically.

### Where does each method do better, and why?

TF-IDF generally performs best when character names are directly mentioned in the question and repeated various times in the overview, which could be because of the fact that specific names are ranked very highly and therefore considered highly indicative of a given film. The embedding search is better when the plot summary and questions are semantically very similar, regardless of word matching.

### Your Part 0 predictions: which held, and which would you change?

They both held because of how the different systems work: TF-IDF is highly dependent on the frequency/rarity of a term, while embedding search looks at the meaning of a sentence.

### How might you combine the two methods?

A fine-tuning of the embeddings model can help producing better predictions.

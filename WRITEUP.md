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

XXXX

### Did the movies you meant come up? What did TF-IDF get right and wrong?

XXXX

## Part 4: The question bank

### Which kind of question did TF-IDF handle best, and which worst? By how much?

XXXX

### The misses you looked at: what do they have in common?

XXXX

## Part 5: Embeddings

### What is a sentence embedding, in your own words?

XXXX

### Where does each method do better, and why?

XXXX

### Your Part 0 predictions: which held, and which would you change?

XXXX

### How might you combine the two methods?

XXXX

# Hangman


### Game rule

When a player plays Hangman, the program randomly selects a secrete word from the word dictionary. Each time, the player guess a letter, if the letter is in the secrete word, the system will return the location of that letter; if it is not, the player lose one chance. In total, the player gets 6 chances of incorrect guesses. In the end, the player either win the game by guessing the word within 6 incorrect guesses or lose.

The dictionary contains 370099 words in total. The success rate is roughly 50%.


### Abstract
Basic idea is to mimic the n-gram model in text mining, but here instead of paritioning sentence into words, I partition the word into n contiguous letters. Then I partition the word to guess in the same way and match the n-gram model. Finally use simple Bayesian probability to decide which letter to guess next. The algorithm gets 50% success rate for 6 chances.

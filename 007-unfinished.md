# 2026-06-18

## Task 1: Niven numbers

Print all the niven numbers from 0 to 50 inclusive, each on their own line. A niven number is a non-negative number that is divisible by the sum of its digits.

### UIUA

Niven ← ▽⊸≡(=0˜◿⟜(/+⊥10))⇡₁

In: 20
Out: [1 2 3 4 5 6 7 8 9 10 12 18 20]

## Task 2: Word ladders

A word ladder is a sequence of words [w0, w1, …, wn] such that each word wi in the sequence is obtained by changing a single character in the word wi-1. All words in the ladder must be valid English words. Given two input words and a file that contains an ordered word list, implement a routine (e.g., find_shortest_ladder(word1, word2, wordlist)) that finds the shortest ladder between the two input words. For example, for the words cold and warm, the routine might return: (“cold”, “cord”, “core”, “care”, “card”, “ward”, “warm”) However, there’s a shortest ladder: (“cold”, “cord”, “card”, “ward”, “warm”).

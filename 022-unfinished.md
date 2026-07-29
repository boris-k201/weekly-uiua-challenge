# 2026-07-02

## Task 1: Sexy prime pairs

Write a script to print first 10 Sexy Prime Pairs. Sexy primes are prime numbers that differ from each other by 6. For example, the numbers 5 and 11 are both sexy primes, because 11 - 5 = 6. The term “sexy prime” is a pun stemming from the Latin word for six: sex. For more information, please checkout wiki page.

### Uiua

```
Prime ← ↧1/×◿⊸(⇡₂ ⌊√)

Primes ← +1⊚≡Prime⇡₁
Primes 100
⊏⊚⊸(≡Prime+6)
≡(&p˜$"_ - _"+6⟜∘)
```

## Task 2: LZW Compression

Write a script to implement Lempel–Ziv–Welch (LZW) compression algorithm. The script should have method to encode/decode algorithm. The wiki page explains the compression algorithm very nicely.

I must confess, it took me many years to get my head around the compression algorithm, I finally understood while doing research for the task. So thanks to Perl Weekly Challenge, I can proudly say that now I understand the compression algorithm. I hope you will enjoy this task as much as I did.

### Uiua

```
# Experimental!

Iteration ← (
  ⍢(-1|=0/+∊□↙)⊸⧻
  ⊙⊙⊙◌◠(˜⊂⊚⌕□↙)
  ⤚(≥+1)⊙⊸⧻
  ⨬(∘|⊙⊙◌◠(˜⊂□↙+1))
  ↘
)

Encode ← (
  []
  ≡(□[+@ ]) ⇡95
  ⍜(⊟₃□⊙□⊙⊙□|↻2)
  ⍢(Iteration|>1⧻)
  ⨬(◌⊙◌⊙◌⟜∘|⊂⊚⌕□)>0⊸⧻
)

# Decode = (

# )

# Encode "Hello, ello"

[40 69 76 76 79 12 0 96 98]
[]
≡(□[+@ ]) ⇡95
⍜(⊟₃□⊙□⊙⊙□|↻2)
```

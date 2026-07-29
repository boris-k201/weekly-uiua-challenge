# 2026-06-25

## Task 1: Pythagoras Pie Puzzle

Pythagoras Pie Puzzle, proposed by Jo Christian Oterhals.

```
At a party a pie is to be shared by 100 guest. The first guest gets 1% of the pie, the second guest gets 2% of the remaining pie, the third gets 3% of the remaining pie, the fourth gets 4% and so on.
```

Write a script that figures out which guest gets the largest piece of pie.

### Uiua

```
⊂100÷100⇡₁100
\(˜-⟜×)
⧈˜-
+1⊢⍖
```

## Task 2: Validating Bitcoin addresses

Write a script to validate a given bitcoin address. Most Bitcoin addresses are 34 characters. They consist of random digits and uppercase and lowercase letters, with the exception that the uppercase letter “O”, uppercase letter “I”, lowercase letter “l”, and the number “0” are never used to prevent visual ambiguity. A bitcoin address encodes 25 bytes. The last four bytes are a checksum check. They are the first four bytes of a double SHA-256 digest of the previous 21 bytes. For more information, please refer wiki page. Here are some valid bitcoin addresses:

```
1BvBMSEYstWetqTFn5Au4m4GFg7xJaNVN2
3J98t1WpEZ73CNmQviecrnyiWrnqRhWNLy
```

# 2026-07-12

## Task 1: Vehicle Identification Numbers

Write a program to validate given Vehicle Identification Number (VIN). For more information, please checkout wikipedia.

### Uiua

```
L ← +@A⊚¬♭↯1_26°⊚-@A"OIUQ"
N ← +@0⇡10
F ← ⊂₃ ⇡₂9⇡₁9 ⇡₁9
W ← [8 7 6 5 4 3 2 10 0 9 8 7 6 5 4 3 2]

ValidateCheckDigit ← (
  ⊙(↻¯8⊂@0)°⊂↻8
  ⨬(-@0|10)⊸=@X
  ⊙(
    ≡(
      ⊸∊L
      ⨬(-@0|-1˜⊏F-@A)
    )
    ◿11/+×W
  )
  =
)

$ 1M8GDM9AXKP042788

⊸(/×[⊃(=17⧻|↧1/×+⊃(∊N|∊L))])
⨬(0|ValidateCheckDigit)
```

## Task 2: Knapsack problem

Write a program to solve Knapsack Problem.

There are 5 color coded boxes with varying weights and amounts in GBP. Which boxes should be choosen to maximize the amount of money while still keeping the overall weight under or equal to 15 kgs?
R: (weight = 1 kg, amount = £1)
B: (weight = 1 kg, amount = £2)
G: (weight = 2 kg, amount = £2)
Y: (weight = 12 kg, amount = £4)
P: (weight = 4 kg, amount = £10)

Bonus task, what if you were allowed to pick only 2 boxes or 3 boxes or 4 boxes? Find out which combination of boxes is the most optimal?

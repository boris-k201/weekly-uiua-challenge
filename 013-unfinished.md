# 2026-06-22

## Task 1: Last Fridays of every month

Write a script to print the date of last Friday of every month of a given year. For example, if the given year is 2019 then it should print the following:

```
2019/01/25
2019/02/22
2019/03/29
2019/04/26
2019/05/31
2019/06/28
2019/07/26
2019/08/30
2019/09/27
2019/10/25
2019/11/29
2019/12/27
```

### Uiua

```
AnchorDays ← [5 3 2 0]
IsLeapYear ← =↧1+0◿400⟜(×≠0◿100⟜(=0◿4))
Months     ← +[31 28 31 30 31 30 31 31 30 31 30 31]↻¯2⊂↯11 0IsLeapYear
DoomsDay ← (
  ⟜(⌊÷12◿100)
  ⟜⊸(⌵-◿100⊙(×12))
  ⊙⊸(⌊÷4⌵)
  (˜⊏AnchorDays(-18⌊÷100))
  ◿7/+⊂₄
)
JanFirst   ← ◿7+1-+3 IsLeapYear⟜DoomsDay
WhichMonth ← /+<0-⊙(\+Months)
LastFridays ← (
  ⟜(↻¯1\+⊏⊙Months ⇡12)
  ⊚≡(=5◿7-2+⊙JanFirst)⇡₁ +365 ⊸⊸IsLeapYear
  ˜⊜□⟜⊸(+1≡WhichMonth)
  ⊙◌
  ≡(˜◿⊣°□)
)
FormatLF ← (
  ⊸LastFridays
  ⬚@0°⋕⇡₁12
  ≡(&p˜⊂⊙°⋕⊂@/˜⊂⊙°⋕⊂@/)
)
FormatLF 2020
# dipdipMonths0 25 2019
```

In: 2022

Out:

```
2020/31/01
2020/28/02
2020/27/03
2020/24/04
2020/29/05
2020/26/06
2020/31/07
2020/28/08
2020/25/09
2020/30/10
2020/27/11
2020/25/12
```

## Task 2: Mutually recursive methods

Write a script to demonstrate Mutually Recursive methods. Two methods are mutually recursive if the first method calls the second and the second calls first in turn. Using the mutually recursive methods, generate Hofstadter Female and Male sequences.

 F ( 0 ) = 1   ;   M ( 0 ) = 0
 F ( n ) = n − M ( F ( n − 1 ) ) , n > 0
 M ( n ) = n − F ( M ( n − 1 ) ) , n > 0.



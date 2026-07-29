# 2026-07-26

## Task 1: Sort Email Addresses

Write a script that takes a list of email addresses (one per line) and sorts them first by the domain part of the email address, and then by the part to the left of the @ (known as the mailbox).

Note that the domain is case-insensitive, while the mailbox part is case sensitive. (Some email providers choose to ignore case, but that’s another matter entirely.)

If your script is invoked with arguments, it should treat them as file names and read them in order, otherwise your script should read email addresses from standard input.
Bonus

Add a -u option which only includes unique email addresses in the output, just like sort -u.
Example

If given the following list:

name@example.org
rjt@cpan.org
Name@example.org
rjt@CPAN.org
user@alpha.example.org

Your script (without -u) would return:

user@alpha.example.org
rjt@cpan.org
rjt@CPAN.org
Name@example.org
name@example.org

With -u, the script would return:

user@alpha.example.org
rjt@CPAN.org
Name@example.org
name@example.org

The following task is submitted by Ryan Thompson,

### Uiua

```
SortEmail ← (
  ⊜□ ⊸≠@\n
  ⊜□+1⊛˜⊏⊙⟜⊏⟜⍏⊸≡(¯⌵⊣⊜□ ⊸≠@@°□)
  ≡(
    □≡(⊏⍏⊸≡(⊏⊚\×⊸≠@@°□)°□)
  )
  /(⊂⊙°□°□)
)

SortEmailU ← (
  SortEmail
  ◴≡(□¯⌵°□)
)

$ name@example.org
$ rjt@cpan.org
$ Name@example.org
$ rjt@CPAN.org
$ user@alpha.example.org
SortEmailU
```

## Task 2: N Queens

A standard 8×8 chessboard has 64 squares. The Queen is a chesspiece that can attack in 8 directions, as shown by the green shaded squares below:

It is possible to place 8 queens on to a single chessboard such that none of the queens can attack each other (i.e., their shaded squares would not overlap). In fact, there are multiple ways to do so, and this is a favourite undergraduate assignment in computer science.

But here at PWC, we’re going to take it into the next dimension!

Your job is to write a script to work with a three dimensional chess cube, M×M×M in size, and find a solution that maximizes the number of queens that can be placed in that cube without attacking each other. Output one possible solution.
Example

A trivial 2×2×2 solution might look like this (1 = queen, 0 = empty):

[
[[1,0],     # Layer 1
[0,0]],

[[0,0],     # Layer 2
[0,0]],
]

### Uiua

```
NDCoordArray ← (
  ♭◡(°△▽)
  ⊸₂≡(
    ⊙⊸(ⁿ⇡)
    ˜◿⌊˜≡(÷)
    □
  )
  ˜↯⊙▽
  ⤸⇌⇡⊸(⧻△)
)
NDCoordArray 2 5
```

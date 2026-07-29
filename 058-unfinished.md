# 2026-07-23

## Task 1: Compare Version

Compare two given version number strings v1 and v2 such that:

    If v1 > v2 return 1
    If v1 < v2 return -1
    Otherwise, return 0

The version numbers are non-empty strings containing only digits, and the dot (".") and underscore ("_") characters. ("_" denotes an alpha/development version, and has a lower precedence than a dot, “.”). Here are some examples:

v1   v2    Result
------ ------ ------
0.1 < 1.1     -1
2.0 > 1.2      1
1.2 < 1.2_5   -1
1.2.1 > 1.2_1    1
1.2.1 = 1.2.1    0

Version numbers may also contain leading zeros. You may handle these how you wish, as long as it’s consistent.

### Uiua

```
# Experimental!

VersionCompare ← (
  ⊜□⊸≠@_
  ⊙(⊜□⊸≠@_)

  ◡(⊃(>0±|˜▽□"0"⌵)-⧻⊙⧻)
  ⨬(˜⊙˜⊂|˜⊂)

  ≡(□⊜⋕⊸≠@.°□)
  ⊙≡(□⊜⋕⊸≠@.°□)

  ◡(⊃(>0±|˜▽0⌵)-⊙(⧻°□⊢)⧻°□⊢)
  ⨬(˜⊙(⊂□˜⊂⊙(°□°⊂))|⊂□˜⊂⊙(°□°⊂))
  join0
  dip(join0)
  drop1/(⊂°□⊙°□)
  dip(drop1/(⊂°□⊙°□))
  ≡(±˜-)
  ⊢⍢(↘1|⨬(0|=0⊢)>1⊸⧻)
)

VersionCompare "0.5.2_2" "0.5_2"
VersionCompare "0.1" "1.1"
VersionCompare "2.0" "1.2"
VersionCompare "1.2" "1.2_5"
VersionCompare "1.2.1" "1.2_1"
VersionCompare "1.2.1" "1.2.1"
```

## Task 2: Ordered Lineup

Write a script to arrange people in a lineup according to how many taller people are in front of each person in line. You are given two arrays. @H is a list of unique heights, in any order. @T is a list of how many taller people are to be put in front of the corresponding person in @H. The output is the final ordering of people’s heights, or an error if there is no solution.

Here is a small example:

    @H = (2, 6, 4, 5, 1, 3) # Heights
    @T = (1, 0, 2, 0, 1, 2) # Number of taller people in front

The ordering of both arrays lines up, so H[i] and T[i] refer to the same person. For example, there are 2 taller people in front of the person with height 4, and there is 1 person in front of the person with height 1.

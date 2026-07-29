# 2026-06-18

## Task 1: Compact number lists

Create a script which takes a list of numbers from command line and print the same in the compact form. For example, if you pass “1,2,3,4,9,10,14,15,16” then it should print the compact form like “1-4,9,10,14-16”.


### Uiua

```
F ← (
  ⊃(=+1°□⊣°□⊣°□⊙°□|∘⊙∘)
  ⨬(□⊂°□|□⊂⊙(□⊂°□)°⊂⌟°□)
)
PrettyPrint ← (
  °□
  =1⊸⧻
  ⨬(˜⊂⊂"-"⊙°⋕⊙°□°⋕°□⊣⟜⊢|°⋕°□)
)

≡□[1 2 3 4 6 8 10 11 12 14 15 16]
⊂ □↯1 °⊂
/F
≡(□ PrettyPrint)°□
/(⊂˜⊂","°□⊙°□)
```

## Task 2: Ramanujan’s constant

Create a script to calculate Ramanujan’s constant with at least 32 digits of precision. Find out more about it here. 

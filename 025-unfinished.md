# 2026-07-07

## Task 1: Head to tail Pokémon names

Generate a longest sequence of the following “English Pokemon” names where each name starts with the last letter of previous name.

audino bagon baltoy banette bidoof braviary bronzor carracosta charmeleon cresselia croagunk darmanitan deino emboar emolga exeggcute gabite girafarig gulpin haxorus heatmor heatran ivysaur jellicent jumpluff kangaskhan kricketune landorus ledyba loudred lumineon lunatone machamp magnezone mamoswine nosepass petilil pidgeotto pikachu pinsir poliwrath poochyena porygon2 porygonz registeel relicanth remoraid rufflet sableye scolipede scrafty seaking sealeo silcoon simisear snivy snorlax spoink starly tirtouga trapinch treecko tyrogue vigoroth vulpix wailord wartortle whismur wingull yamask

The above names borrowed from wiki page.

## Task 2: Chaocipher implementation

Create script to implement Chaocipher. Please checkout wiki page for more information.

We decided to put the optional API task on hold for the time being, while we are working on the format.

### Uiua

```
PermuteLeft ← (
  ÷2⊸⧻
  ⊃(↙|↘)
  ⊙(⊂⊙⇌°⊂⇌)
  ⊂
)

PermuteRight ← (
  ↻3
  ÷2⊸⧻
  -1
  ⊃(↙|↘)
  ⇌⊂⊙(⇌)°⊂
  ⊂
  ↻¯2
)

Encrypt ← (
  ⊃(◌⊙∘|↻⊙◌|⊢↻⊙◌)⟜↻⊸(⊚⌕)⊢
  ⊙PermuteLeft
  PermuteRight
)
Decrypt ← (
  ⊃(◌⊙∘|↻⊙◌|⊢↻⊙◌)⟜↻⊸(⊚⌕)⊢
  PermuteLeft
  ⊙PermuteRight
)

"cnkjwhugvfbazomlyxitsrqdep"
"ayznbqdsefghlwikcmoprtuvjx"
"message"
⍢(↘1⟜Encrypt|>0⧻)

"ayznbqdsefghlwikcmoprtuvjx"
"cnkjwhugvfbazomlyxitsrqdep"
"xuyktod"
⍢(↘1⟜Decrypt|>0⧻)
```

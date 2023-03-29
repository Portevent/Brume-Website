---
title: HandSpell
path: /UI
alias: 
- Hand Spell
tag: 
- class
---
A HandSpell is a MonoBehaviour object that link a spell in the player's DeckManager to UI Button
It manage the icon and cooldown displayed
Currently the cooldown system is based on local cooldown value saved within HandSpell. Probably need to rework this
(this can cause glitch and abuse, and anyway not a good pattern

---
# Summary :
name|description
----|----
[Setup]({{< ref "#setup" >}}) | `Assign the Spell sprite to the button and set the cooldown to 0`
[SelectSpell]({{< ref "#selectspell" >}}) | `Select this HandSpell as the active HandSpell.
This will notify the DeckManager`
[ApplyCooldown]({{< ref "#applycooldown" >}}) | `Apply the cooldown of the selected spell to the HandSpell`

---
# Functions :

---
### Setup
Assign the Spell sprite to the button and set the cooldown to 0

---
### SelectSpell
Select this HandSpell as the active HandSpell.
This will notify the DeckManager

---
### ApplyCooldown
Apply the cooldown of the selected spell to the HandSpell

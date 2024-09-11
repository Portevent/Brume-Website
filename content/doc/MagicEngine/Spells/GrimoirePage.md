---
title: GrimoirePage
path: /MagicEngine/Spells
alias: 
- Grimoire Page
tag: 
- class
---
A Grimoire Page represent a Spell within a Grimoire, tracking its cooldown  

![GrimoirePage](GrimoirePage.svg "GrimoirePage")

---
# Summary :
name|description
----|----
[AddCooldown]({{< ref "#addcooldown" >}}) | `Add cooldown duration`
[ReduceCooldown]({{< ref "#reducecooldown" >}}) | `Reduce cooldown duration`
[ApplyCooldown]({{< ref "#applycooldown" >}}) | `Set a page cooldown to its spell cooldown duration`

---
# Functions :

---
### AddCooldown
Add cooldown duration

#### Parameters
name|type|description
-----|-----|-----
**value**|`int`|number of turn to add

---
### ReduceCooldown
Reduce cooldown duration

#### Parameters
name|type|description
-----|-----|-----
**value**|`int`|number of turn to remove (-1 to reset it to 0)

---
### ApplyCooldown
Set a page cooldown to its spell cooldown duration

#### Return
- `int` : the cooldown duration applied

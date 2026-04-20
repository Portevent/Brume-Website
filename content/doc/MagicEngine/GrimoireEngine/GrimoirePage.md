---
title: GrimoirePage
path: /MagicEngine/GrimoireEngine
alias: 
- Grimoire Page
tag: 
- class
---
A Grimoire Page is a spell entry in a grimoire, with an attached cooldown  

![GrimoirePage](GrimoirePage.svg "GrimoirePage")

---
# Summary :
name|description
----|----
[AddCooldown]({{< ref "#addcooldown" >}}) | `Add cooldown duration`
[ClearCooldown]({{< ref "#clearcooldown" >}}) | `Clear cooldown duration`
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
### ClearCooldown
Clear cooldown duration

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

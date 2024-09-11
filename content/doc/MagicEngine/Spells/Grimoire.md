---
title: Grimoire
path: /MagicEngine/Spells
alias: 
- Grimoire
tag: 
- class
---
A grimoire represent the ability of entity to cast spell  
Grimoire hold a list of usable spell and their cooldown.  

![Grimoire](Grimoire.svg "Grimoire")

---
# Summary :
name|description
----|----
[Awake]({{< ref "#awake" >}}) | `Take a list of spells and create a Grimoire with theses spells in the same order (0 to n)`
[AddSpell]({{< ref "#addspell" >}}) | `Add a new Page with specified Spell`
[ReduceAllCooldown]({{< ref "#reduceallcooldown" >}}) | `Reduce all cooldown durations`
[GetFirstValidPage]({{< ref "#getfirstvalidpage" >}}) | `Get the first page that is not on cooldown`
[GetFirstValidPageOnTarget]({{< ref "#getfirstvalidpageontarget" >}}) | `Get the first page that is not on cooldown and can be cast on target`
[GetFirstValidPageOnCell]({{< ref "#getfirstvalidpageoncell" >}}) | `Get the first page that is not on cooldown and can be cast on cell`

---
# Functions :

---
### Awake
Take a list of spells and create a Grimoire with theses spells in the same order (0 to n)

---
### AddSpell
Add a new Page with specified Spell

#### Parameters
name|type|description
-----|-----|-----
**spell**|[Spell]({{< ref "Spell" >}})|Spell to add to the Grimoire
**position**|`int`|index where to set the Page (0 by default, first page)
**cooldown**|`int`|cooldown of the Spell once in the Grimoire

#### Return
- [GrimoirePage]({{< ref "GrimoirePage" >}}) : Return the Page linked to the Spell

---
### ReduceAllCooldown
Reduce all cooldown durations

#### Parameters
name|type|description
-----|-----|-----
**value**|`int`|number of turn to remove (-1 to reset it to 0)

---
### GetFirstValidPage
Get the first page that is not on cooldown

#### Return
- `Page` : Page, or null if all are on cooldown

---
### GetFirstValidPageOnTarget
Get the first page that is not on cooldown and can be cast on target

#### Parameters
name|type|description
-----|-----|-----
**target**|[Entity]({{< ref "Entity" >}})|Entity targeted

#### Return
- `Page` : Page, or null if all are on cooldown

---
### GetFirstValidPageOnCell
Get the first page that is not on cooldown and can be cast on cell

#### Parameters
name|type|description
-----|-----|-----
**target**|[Coordinate]({{< ref "Coordinate" >}})|Cell targeted

#### Return
- `Page` : Page, or null if all are on cooldown

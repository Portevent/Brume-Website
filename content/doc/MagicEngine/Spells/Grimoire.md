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
![Grimoire.svg]({{< ref "Grimoire.svg" >}})

---
# Summary :
name|description
----|----
[Awake]({{< ref "#awake" >}}) | `Take a list of spells and create a Grimoire with theses spells in the same order (0 to n)`
[AddSpell]({{< ref "#addspell" >}}) | `Add a spell to a position`
[RemoveSpell]({{< ref "#removespell" >}}) | `Remove Spell from the Grimoire`
[SetCooldown]({{< ref "#setcooldown" >}}) | `Set the Cooldown of specified to value`
[GetCooldown]({{< ref "#getcooldown" >}}) | `Return the cooldown of a Spell`
[GetCooldownEvent]({{< ref "#getcooldownevent" >}}) | `Return the CooldownEvent of a spell`
[ReduceAllCooldown]({{< ref "#reduceallcooldown" >}}) | `Reduce all cooldown duration`
[ApplyCooldown]({{< ref "#applycooldown" >}}) | `Set a spell cooldown to its cooldown duration`
[GetFirstValidSpell]({{< ref "#getfirstvalidspell" >}}) | `Get the first spell that is not on cooldown`
[GetFirstValidSpellOn]({{< ref "#getfirstvalidspellon" >}}) | `Get the first spell that is not on cooldown and can be cast on target`
[GetSpells]({{< ref "#getspells" >}}) | `Return an Iterator of all spells`

---
# Functions :

---
### Awake
Take a list of spells and create a Grimoire with theses spells in the same order (0 to n)

---
### AddSpell
Add a spell to a position

#### Parameters
name|type|description
-----|-----|-----
**spell**|[Spell]({{< ref "Spell" >}})|Spell to add to the Grimoire
**position**|`int`|index where to set the Spell
**cooldown**|`int`|cooldown of the Spell once in the Grimoire

#### Return
- `CooldownEvent` : Return the CooldownEvent linked to the Spell

---
### RemoveSpell
Remove Spell from the Grimoire

#### Parameters
name|type|description
-----|-----|-----
**spell**|[Spell]({{< ref "Spell" >}})|Spell to remove

---
### SetCooldown
Set the Cooldown of specified to value

#### Parameters
name|type|description
-----|-----|-----
**spell**|[Spell]({{< ref "Spell" >}})|Spell to which the cooldown is applied
**value**|`int`|duration of the cooldown

#### Return
- `int` : cooldown applied

---
### GetCooldown
Return the cooldown of a Spell

#### Parameters
name|type|description
-----|-----|-----
**spell**|[Spell]({{< ref "Spell" >}})|Spell to check
**defaultCooldown**|`int`|value to return if not present

#### Return
- `int` : cooldown (turns count)

---
### GetCooldownEvent
Return the CooldownEvent of a spell

#### Parameters
name|type|description
-----|-----|-----
**spell**|[Spell]({{< ref "Spell" >}})|Spell to check

#### Return
- `CooldownEvent` : CooldownEvent of the spell

---
### ReduceAllCooldown
Reduce all cooldown duration

#### Parameters
name|type|description
-----|-----|-----
**value**|`int`|number of turn to remove (-1 to reset it to 0)

---
### ApplyCooldown
Set a spell cooldown to its cooldown duration

#### Parameters
name|type|description
-----|-----|-----
**spell**|[Spell]({{< ref "Spell" >}})|Spell to apply cooldown on
**duration**|`int`|duration to apply (-1 to use the spell cooldown duration)

#### Return
- `int` : the cooldown duration applied

---
### GetFirstValidSpell
Get the first spell that is not on cooldown

#### Return
- [Spell]({{< ref "Spell" >}}) : Spell, or null if all are on cooldown

---
### GetFirstValidSpellOn
Get the first spell that is not on cooldown and can be cast on target

#### Parameters
name|type|description
-----|-----|-----
**caster**|[Entity]({{< ref "Entity" >}})|Entity casting
**target**|[Entity]({{< ref "Entity" >}})|Entity targeted

#### Return
- [Spell]({{< ref "Spell" >}}) : Spell, or null if all are on cooldown

---
### GetSpells
Return an Iterator of all spells

#### Return
- `IEnumerable` : IEnumerable with all spells
